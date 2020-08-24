<template>
<div>
  <v-container fluid class="pa-0">
    <Hero />
  </v-container>
  <v-container fluid class="pa-2">
     <About />
  </v-container>
  <v-container fluid class="pa-2">
   <v-divider/>
     <Project />
  </v-container>
  <v-container fluid class="pa-5">
    <v-divider/>
     <Solution />
  </v-container>
  <!-- <v-container fluid class="">
     <Contact />
  </v-container> -->
</div>
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

