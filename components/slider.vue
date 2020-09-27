<template>
  <v-container fluid class="">
    <v-layout row wrap justify-center align-center>
      <v-flex xs10 sm12 md12 lg12>
        <v-row class="fill-height text-center" align="center" justify="center">
          <v-col md="6" sm="6" lg="6" v-for="card in cards" :key="card.title" class="item">
            <v-card height="150" outlined tile width="400" elevation class="pa-1">
              <h3>{{card.title}}</h3>

              <p>{{card.info}}</p>
            </v-card>
          </v-col>
        </v-row>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<style scoped>
h2 {
  font-size: 1.35em;
  letter-spacing: 0.01em;
  padding: 0.7em 0 0.7em 0;
  line-height: 1.4em;
  font-weight: 400;
  text-transform: uppercase;
  color: #38506d;
}
h3 {
  text-transform: capitalize;
}

p {
  color: #002155;
  font-size: 14px;
  font-weight: 700;
}
item:hover {
  border-color: #002155;
}
.bg {
  padding-bottom: 50px;
}
</style>

<script>
export default {
  data: () => ({
    cards: [
      {
        title: 'Home Security System',
        info:
          'Alarm Systems, Automated Doors, CCTV, Electric Fence, Automated Gates',
      },

      {
        title: 'Access Control',
        info:
          'RFID key cards, Phone Entry Systems, magnetic door locks, event monitoring, time attendance',
      },
      {
        title: 'Solar Energy',
        info:
          'solar lighting, solar panels, system design, inverter, batteries',
      },
      {
        title: 'networking',
        info:
          'computer based tesing, call centres intercom phones, VoLP, fibre optic, VSAT installation',
      },
      // {
      //   title: 'internet services',
      //   info: 'internet streaming, web development, web hosting, bulk sms',
      // },

      // {
      //   title: 'GPS Tracking',
      //   info:
      //     'vehicle tracking, human locators, fleet management, equipment monitoring, covert tracking',
      // },
    ],
  }),
}
</script>