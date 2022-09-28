<template>
  <div>
    <h2 class="text-h2 text-center mt-10 mb-6">
      Our Process
    </h2>

    <v-timeline
        style="max-width: 1000px;"
        class="mx-auto"
        align-top
        :dense="$vuetify.breakpoint.smAndDown"
    >
      <v-timeline-item
          v-for="({ title, description, color, icon }, i) in items"
          :key="title"
          :color="color"
          :icon="icon"
          fill-dot
      >
        <v-card
          :color="color"
          dark
        >
          <v-card-title class="text-h6">
            {{ title }}
          </v-card-title>
          <v-card-text class="white text--primary pt-3">
            <span class="body-2">{{ description }}</span>
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </div>
</template>

<script>
export default {
  name: 'Timeline',
  data: () => ({
    items: [
      {
        color: 'red lighten-2',
        icon: 'mdi-head-snowflake',
        title: 'Requirements',
        description: 'Our outsource web development company gathers requirements that describe the business needs of your project. We decompose the specification into small tasks to estimate the scope precisely and prepare a strict delivery plan for your approval.'
      },
      {
        color: 'purple darken-1',
        icon: 'mdi-clipboard-list-outline',
        title: 'Design',
        description: 'At this stage, you will get two prototypes. The first one is wireframes that allow visualizing project functionality and user flow. The next step is to create an interactive UI prototype that looks almost like the real product.'
      },
      {
        color: 'green lighten-1',
        icon: 'mdi-account-group',
        title: 'Development',
        description: 'There are no two similar projects. We always develop a personal approach to each project we take. Our practices like Continuous integration, code reviews, and pair programming let the team combine speed and agility with a focus on quality.'
      },
      {
        color: 'indigo',
        icon: 'mdi-test-tube',
        title: 'Testing',
        description: 'Software development can’t do without quality assurance. Each project we deliver is precisely tested either manually or automatically. Quality assurance is one of our main values since it’s the basis of our client’s reputation. '
      },
      {
        color: 'orange',
        icon: 'mdi-truck-delivery-outline',
        title: 'Delivery',
        description: 'With Devox Software, your project will be released on time and budget. Our PMs control developers’ performance so you will get your web project done according to the plan. If needed, our team will provide ongoing support for your project.'
      },
    ],
  }),
}
</script>

<style scoped>

</style>
