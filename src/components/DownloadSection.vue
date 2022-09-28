<template>
  <section id="download">
      <v-container class="pa-12">
          <v-row>
            <v-col
                v-for="({ title, description }, i) in items"
                :key="i"
                cols="12"
                md="4"
            >
              <v-item>
                <v-card height="100%">
                  <div class="our-services__item--bookmark">
                    <span>0{{ i + 1 }}</span>
                    <svg width="54" height="145" viewBox="0 0 54 145" fill="none" xmlns="http://www.w3.org/2000/svg" version="1.1">
                      <g filter="url(#filter_service_2)">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M0 8.72983C0 4.52088 4.22065 1.62004 8.15007 3.1283L50.1501 19.2494C52.4692 20.1396 54 22.3669 54 24.851V145L1.28797 63.7218C0.447334 62.4256 0 60.9137 0 59.3688L0 8.72983Z" fill="url(#gradient_service_2)"></path>
                      </g>
                      <defs>
                        <filter id="filter_service_2" x="-12" y="-5.27588" width="78" height="166.276" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                          <feFlood flood-opacity="0" result="BackgroundImageFix"></feFlood>
                          <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 0"></feColorMatrix>
                          <feOffset dy="4"></feOffset>
                          <feGaussianBlur stdDeviation="6"></feGaussianBlur>
                          <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.1 0"></feColorMatrix>
                          <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow"></feBlend>
                          <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow" result="shape"></feBlend>
                        </filter>
                        <linearGradient id="gradient_service_2" x1="0" y1="0" x2="0" y2="145" gradientUnits="userSpaceOnUse">
                          <stop stop="" offset="0" stop-color="#a74ef4"></stop>
                          <stop offset="1" stop-color="#823df7"></stop>
                        </linearGradient>
                      </defs>
                    </svg>
                  </div>
                  <v-card-title>
                    {{ title }}
                  </v-card-title>
                  <v-card-text>
                    {{ description }}
                  </v-card-text>
                </v-card>
              </v-item>
            </v-col>
          </v-row>
      </v-container>
  </section>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        title: 'Front-End Development',
        description: 'Build your brand awareness and increase sales by mere internet presence. Devox Software, a professional outsource web dev company, will create an eye-catching responsive website according to your requirements. Be it a landing or a complex e-store, we can do it all.'
      },
      {
        title: 'Full-Stack Development',
        description: 'Full-stack developers are good at client and server side - they understand customer needs and work with databases and hostings. Our main specialization is Angular and .NEt, but we also deal with PHP, Python and many others - just contact us and ask about the needed one.'
      },
      {
        title: 'Mobile App Development',
        description: 'Came up with an idea of a mobile app, but don’t know how to develop it? We have both part-time and dedicated mobile developers for short-term and long-lasting projects. We don\'t limit ourselves by one technology - you will get a software engineer with the required tech stack.'
      },
      {
        title: 'CMS Development',
        description: 'We analyze your business needs and select the best UX solutions. Our IT outsourcing company makes it easy for you to change content - texts, images, videos, etc. without programmers\' help. Our main focus is WordPress, however, we can also develop bespoke CMS if your business requires it.'
      },
      {
        title: 'E-commerce Development',
        description: 'Devox Software can provide you with a ready-to-go team at an affordable cost for small retailers, startups, SMBs or enterprises. In our talent pool, there are web developers with relevant experience in the e-commerce industry.'
      },
      {
        title: 'Custom Web Development',
        description: 'Wanna add distinctive features to your site or app? We appreciate personal approach and bespoke web solutions. Our project-based or dedicated web developers will listen to your demands and suggest the ways to carry it out.'
      },
    ],
  }),
}
</script>

<style scoped>
.our-services__item--bookmark {
  position: absolute;
  top: -24px;
  right: 0;
}

.our-services__item--bookmark span {
  position: absolute;
  font-size: 30px;
  font-weight: bold;
  font-family: "Poppins",sans-serif;
  color: #fff;
  top: 35%;
  left: 50%;
  transform: translate(-50%, -50%);
}

#download {
  background-image: url("~@/assets/img/bgDownload.jpg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  min-height: 500px;
}

#download .container,
#download .row {
  min-height: 100%;
}
</style>
