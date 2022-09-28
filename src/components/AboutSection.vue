<template>
  <section id="about">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
              <h2 class="text-h2 mb-4">
                About us
              </h2>
              <p class="body-1">
                Hardly any business can do without a website or mobile application. If you need the one too, Devox Software is the right partner for you. Our outsourcing web development company specializes in both front-end and back-end solutions, so you will get convenient and user-friendly pages without setting up a full IT department in your office.
              </p>
              <p class="body-1">
                Instead of spending time on recruiting, extending office and buying extra devices, you can just get your software done hassle-free. Devox Software takes all administrative responsibilities as well as providing you with the required web developers.
                Our engagement models can be adapted to any business – part-time programmers, dedicated teams and up to offshore R&D center.
              </p>
              <p class="body-1">
                Not sure what to choose? Drop us a line, tell us about your project and get a free consultation!
              </p>
            </v-col>
            <v-col cols="12" md="5" class="d-none d-md-flex pt-15">
              <v-img
                src="@/assets/img/ill1.svg"
                class="d-block mx-auto"
                max-width="400px"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>

      <h2 class="text-h2 text-center mt-15 mb-4">
        Technologies
      </h2>
      <div
          class="mx-auto mt-15 mb-15"
          style="max-width: 1200px;"
      >
        <v-slide-group
            multiple
            show-arrows
        >
          <v-slide-item
              v-for="item of items"
              :key="item.src"
          >
            <img class="mx-4"
              :src="item.src"
              alt="technology"
              width="60"
              height="60"
            />
          </v-slide-item>
        </v-slide-group>
      </div>
    </v-container>
  </section>
</template>

https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original-wordmark.svg
<script>
export default {
  data: () => ({
    items: [
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nuxtjs/nuxtjs-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-plain.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/d3js/d3js-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/electron/electron-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/gulp/gulp-plain.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-plain-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original-wordmark.svg'
      },
      {
        src: 'https://raw.githubusercontent.com/devicons/devicon/master/icons/symfony/symfony-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/webpack/webpack-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redux/redux-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nginx/nginx-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sass/sass-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dart/dart-original-wordmark.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg'
      },
      {
        src: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nestjs/nestjs-plain-wordmark.svg'
      },
    ]
  }),
};
</script>

<style scoped>
#about {
  background-color: #f4f7f5;
}
</style>
