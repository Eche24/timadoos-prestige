<template>
  <v-container fluid class="pa-0">
    <v-layout row wrap justify-center align-center>
      <v-flex xs12 md10 lg10 sm10>
        <ProjectHero />
        <WorkOn />
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
import ProjectHero from '~/components/projects/projectHero'
import WorkOn from '~/components/projects/workOn'
export default {
  components: {
    ProjectHero,
    WorkOn
  }
  ,
   head () {
    return {
      title: 'Project',

    }
  }
}
</script>