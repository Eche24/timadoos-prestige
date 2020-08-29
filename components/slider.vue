<template>
  <v-card flat max-width="564" tile>
    <v-window v-model="onboarding" reverse>
      <v-window-item v-for="card in cards" :key="card.title">
        <v-card flat width="600" height="400">
          <!-- <v-row class="fill-height text-center pa-2" align="center" justify="center" > -->
          <v-img class="white--text align-end text-center" height="250px" :src="card.img">
          </v-img>
          <v-card-text>
            <h3>{{card.title}}</h3>
            <p>{{card.info}}</p>
          </v-card-text>
          <!-- </v-row> -->
        </v-card>
      </v-window-item>
    </v-window>

    <v-card-actions class="justify-space-between">
      <v-btn text @click="prev">
        <v-icon>mdi-chevron-left</v-icon>
      </v-btn>
      <v-btn text @click="next">
        <v-icon>mdi-chevron-right</v-icon>
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    length: 11,
    onboarding: 0,
    cards: [
      {
        title: 'Home Security System',
        info:
          'Alarm Systems, Automated Doors, CCTV, Electric Fence, Automated Gates',
        img: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1598260523/timadoos/Inverter_P_H_20170728_145142_vheij1.jpg',
      },

      {
        title: 'Access Control',
        info:
          'RFID key cards, Phone Entry Systems, magnetic door locks, event monitoring, time attendance',
        img: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872582/timadoos/project-3_wl8zzo.png',
      },
      {
        title: 'Solar Energy',
        info:
          'solar lighting, solar panels, system design, inverter, batteries',
        img:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1598260381/timadoos/81662683_966333667081553_7574934606210662400_n_bzhx3f.jpg',
      },
      {
        title: 'networking',
        info:
          'computer based tesing, call centres intercom phones, VoLP, fibre optic, VSAT installation',
          img: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1598731129/timadoos/timadoo-2_bocgah.jpg'
      },
      {
        title: 'internet services',
        info: 'internet streaming, web development, web hosting, bulk sms',
        img: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872582/timadoos/project-3_wl8zzo.png',
      },

      {
        title: 'GPS Tracking',
        info:
          'vehicle tracking, human locators, fleet management, equipment monitoring, covert tracking',
        img: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872582/timadoos/project-3_wl8zzo.png',
      },
    ],
  }),

  methods: {
    next() {
      this.onboarding =
        this.onboarding + 1 === this.length ? 0 : this.onboarding + 1
    },
    prev() {
      this.onboarding =
        this.onboarding - 1 < 0 ? this.length - 1 : this.onboarding - 1
    },
  },
}
</script>
<style scoped>
h2,
h3 {
  font-size: 1.35em;
  letter-spacing: 0.01em;
  padding: 0.7em 0 0.7em 0;
  line-height: 1.4em;
  font-weight: 400;
  text-transform: uppercase;
  color: #38506d;
}
/* h2 {
} */
/* h3 {
  color: #ff6000;
} */
p {
  margin: 0 0 1em 0;
  font-size: 1.1em;
  line-height: 1.8em;
  font-weight: 600;
  text-transform: capitalize;
}
</style>