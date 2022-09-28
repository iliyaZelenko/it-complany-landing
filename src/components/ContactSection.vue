<template>
  <section class="pt-16 pb-16" id="contact">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row justify="center">
            <v-col cols="12" sm="5">
              <h1 class="font-weight-light display-1">
                Contact us
              </h1>
              <h3 class="font-weight-light mt-3">
                Got a project or partnership in mind?
              </h3>
              <h3 class="font-weight-light mt-3">
                Phone: +xx (xx) xxxxx-xxxx
              </h3>
              <h3 class="font-weight-light">
                Email: email@email.com
              </h3>
            </v-col>
            <v-col cols="12" sm="7">
              <v-form ref="form" v-model="valid" :lazy-validation="lazy">
                <v-text-field
                  v-model="name"
                  :rules="nameRules"
                  label="Name"
                  required
                />

                <v-text-field
                  v-model="email"
                  :rules="emailRules"
                  label="E-mail"
                  required
                />

                <v-textarea
                  v-model="textArea"
                  :rules="textAreaRules"
                  label="Message"
                  required
                />

                <v-btn
                  :disabled="loading || !valid"
                  color="primary"
                  :dark="valid"
                  rounded
                  block
                  class="mt-3"
                  @click="submit"
                >
                  Submit
                </v-btn>
              </v-form>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <div class="svg-border-waves text-white">
      <v-img src="~@/assets/img/borderWavesBlue.svg"/>
    </div>
    <v-snackbar
        v-model="snackbar.enabled"
        timeout="3000"
        right
        top
        :color="snackbar.color"
    >
      {{ snackbar.text }}

      <template v-slot:action="{ attrs }">
        <v-btn
            text
            v-bind="attrs"
            @click="snackbar.enabled = false"
        >
          Close
        </v-btn>
      </template>
    </v-snackbar>
  </section>
</template>

<style scoped>
#contact {
  background-color: #f4f7f5;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}

</style>

<script>
// import {db} from '@/main'

export default {
  data: () => ({
    loading: false,
    valid: true,
    name: "",
    nameRules: [
      (v) => !!v || "The name field is required",
      (v) => (v && v.length >= 2) || "The name must be longer than 2 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "The email field is mandatory",
      (v) => /.+@.+\..+/.test(v) || "Email must be valid",
    ],
    textArea: "",
    textAreaRules: [
      (v) => !!v || "Text field is required",
      (v) => (v && v.length >= 10) || "Minimum of 10 characters",
    ],
    lazy: false,
    snackbar: {
      enabled: false,
      text: '',
      color: ''
    }
  }),
  methods: {
    async submit() {
      this.loading = true;

      fetch('https://ro-charity-bot.glitch.me/contact-us', {
        method: 'POST',
        headers: {
          'Accept': 'application/json',
          'Content-Type': 'application/json'
        },
        body: JSON.stringify({
          name: this.name,
          email: this.email,
          message: this.textArea,
        }),
      })
        .then((response) => {
          console.log(response)
          if (response.ok) {
            return response.json();
          }
          return Promise.reject(response);
        })
        .then((json) => {
          this.loading = false;

          this.snackbar.text = "Message sent successfully"
          this.snackbar.color = "green"
          this.snackbar.enabled = true
          this.name = '';
          this.email = '';
          this.textArea = '';

          this.$refs.form.reset()
        })
        .catch((response) => {
          console.log(response)

          this.loading = false;
          this.snackbar.text = "Error sending message"
          this.snackbar.color = "red"
          this.snackbar.enabled = true
        });


      /*db.collection("contactData").add({
        name: this.name,
        email: this.email,
        message: this.textArea
      }).then(() => {
        this.snackbar.text = "Mensagem enviada com sucesso"
        this.snackbar.color = "success"
        this.snackbar.enabled = true
      }).catch(() => {
        this.snackbar.text = "Erro ao enviar mensagem"
        this.snackbar.color = "danger"
        this.snackbar.enabled = true
      })*/
    }
  }
};
</script>
