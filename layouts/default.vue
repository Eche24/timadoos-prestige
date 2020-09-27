<template>
  <v-app>
   <Nav/>
    <v-main class="">
        <nuxt />
    </v-main>
    <Contact  />
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