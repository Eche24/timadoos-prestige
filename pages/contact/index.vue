<template>
  <v-container fluid class="pt-0 pb-0" >
    <v-layout justify-center row wrap align-center style="background-color: #fcfcfc;">
      <v-flex xs12 md10 lg10 sm10>
        <Map />
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
import Map from '@/components/map.vue'
export default {
  components: {
    Map,
  },
  head() {
    return {
      title: 'Contact',
    }
  },
}
</script>
