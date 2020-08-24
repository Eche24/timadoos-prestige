<template>
  <v-container fluid>
    <v-layout row wrap justify-center align-center>
      <v-flex xs10 sm10 md10 lg10>
        <h2>Below are examples of some of our most recent work:</h2>
        <v-row class="fill-height text-center" align="center" justify="center">
          <v-col md="4" sm="4" lg="4" v-for="card in cards" :key="card.title">
            <v-card height="300" outlined tile width="600" elevation>
              <v-img :src="card.src" height="100px"></v-img>
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
h2,
h3 {
  font-size: 1.35em;
  letter-spacing: 0.01em;
  padding: 0.7em 0 0.7em 0;
  line-height: 1.4em;
  font-weight: 400;
  text-transform: uppercase;
}
h2 {
  color: #38506d;
}
h3 {
  color: #ff6000;
}
p {
  margin: 0 0 1em 0;
  font-size: 1.1em;
  line-height: 1.8em;
  font-weight: 600;
  text-transform: capitalize;
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
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872014/timadoos/timadoos-project_b0sv3x.png',
      },

      {
        title: 'Access Control',
        info:
          'RFID key cards, Phone Entry Systems, magnetic door locks, event monitoring, time attendance',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872014/timadoos/timadoos-project_b0sv3x.png',
      },
      {
        title: 'Solar Energy',
        info:
          'solar lighting, solar panels, system design, inverter, batteries',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872014/timadoos/timadoos-project_b0sv3x.png',
      },
      {
        title: 'networking',
        info:
          'computer based tesing, call centres intercom phones, VoLP, fibre optic, VSAT installation',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872014/timadoos/timadoos-project_b0sv3x.png',
      },
    ],
  }),
}
</script>