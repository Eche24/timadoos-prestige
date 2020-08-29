<template>
  <v-container fluid class="pa-0">
    <AboutHero />
    <!-- <v-layout row wrap justify-center align-center fill-height>
      <v-flex xs12 sm11 md11 lg11> -->
        <WhyUs />
      <!-- </v-flex>
    </v-layout> -->
  </v-container>
</template>
<script>
import AboutHero from '~/components/about/aboutHero'
import WhyUs from '~/components/about/whyUs'
export default {
  components: {
    AboutHero,
    WhyUs,
  },

  head() {
    return {
      title: 'About',
    }
  },
}
</script>