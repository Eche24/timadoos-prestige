<template>
  <v-container fluid class="" style="background-color: #f7f7f7;" >
    <v-layout row wrap justify-center align-center fill-height>
      <v-flex xs12 sm11 md11 lg11>
        <ServiceHero />
        <ServicesOffer />
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
import ServiceHero from '~/components/services/serviceHero'
import ServicesOffer from '~/components/services/servicesOffer'
export default {
  components: {
    ServiceHero,
    ServicesOffer,
  }
  ,
   head () {
    return {
      title: '  Services',

    }
  }
}
</script>