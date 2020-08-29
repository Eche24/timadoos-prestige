<template>
  <v-container fluid class="pa-0">
    <!-- <v-container fluid class="pa-0"> -->
    <Hero />
    <!-- </v-container> -->
    <!-- <v-container fluid class="pa-2"> -->
    <About />
    <!-- </v-container> -->
    <!-- <v-container fluid class="" > -->
    <!-- <v-divider inset style="background: #e0edf6 url(../img/content-bg.jpg) top center;" /> -->

    <Project />
    <!-- </v-container> -->
    <!-- <v-container fluid class="pa-5" > -->
    <Solution />
    <!-- </v-container> -->
    <!-- <v-container fluid class="">
     <Contact />
    </v-container>-->
  </v-container>
</template>
<script>
import Hero from '../components/hero.vue'
import About from '../components/About.vue'
import Project from '../components/Project.vue'
import Solution from '../components/Solution.vue'
// import Contact from '../components/Contact.vue'
export default {
  components: {
    Hero,
    About,
    Project,
    Solution,
  },
}
</script>

