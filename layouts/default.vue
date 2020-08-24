<template>
  <v-app >
   <Nav />
    <v-main class="pa-0">
      <!-- <v-container fluid> -->
        <nuxt />
      <!-- </v-container> -->
    </v-main>
    <!-- <v-divider/> -->
    <Contact />
    <Footer />
  </v-app>
</template>

<script>
import Nav from '../components/nav'
import Footer from '../components/footer'
import Contact from '../components/contact'
export default {
  components: {
    Nav,
    Footer,
    Contact
  }
}
</script>