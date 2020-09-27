<template>
  <v-container fluid class="pb-0 pt-0" style="background-color: #f7f7f7;">
    <v-layout row justify-center align-center wrap fill-height class="pa-4">
      <v-flex xs10 sm10 md10 lg10>
        <v-row>
          <v-col cols="12" md="6">
            <v-card class="pa-2" flat style="background-color: #f7f7f7;">
              <h2>services</h2>
              <v-card-text>
                <p>We provide security solutions that suit your specific needs and business environment and advise on the best technical and operational systems required to achieve your overall objectives.</p>
                <p>Your project could be anything from needing to implement new technologies, upgrading your existing security systems, understanding what your risks are or to writing an emergency management plan.</p>
              </v-card-text>
              <v-card-actions class="launch-wrap">
                <a
                  href="/services"
                  target="_blank"
                  rel="noopener noreferrer"
                >explore all our services</a>
              </v-card-actions>
            </v-card>
          </v-col>
          <v-col cols="12" md="6">
            <h2 class>Most Popular Security Serviced</h2>
            <!-- <v-card class="pa-2" outlined tile max-width> -->
              <Slider />
            <!-- </v-card> -->
          </v-col>
        </v-row>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
import Slider from '../components/slider.vue'

export default {
  components: {
    Slider,
  },
}
</script>
<style scoped>
.launch-wrap a {
  color: #333;
  min-width: 12em;
  border-bottom: 1px solid #bbcedb;
  display: inline-block;
  padding: 0.4em 1em;
}
.launch-wrap a::after {
  content: ' →';
}
h2 {
  text-transform: uppercase;
  color: #002155;
  font-size: 22px;
}
</style>