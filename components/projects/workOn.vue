<template>
  <v-container fluid class="bg">
    <v-layout row wrap justify-center align-center>
      <v-flex xs10 sm10 md10 lg10>
        <h2>Below are examples of some of our most recent work:</h2>
        <v-row>
          <v-col cols="12" sm="6" md="6" v-for="card in cards" :key="card.title">
            <v-card class="pa-3 mx-auto" flat max-width="440">
              <v-img :src="card.src" height="200px"></v-img>
              <h4 class="pt-3">Client: {{card.title}}</h4>

              <P>
                <strong>Services:</strong>
                {{card.services}}
              </P>
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
  color: #38506d;
  text-transform: uppercase;
}

p {
  color: #848787;
  font-size: 12px;
  line-height: 1.33;
}
h4 {
  font-size: 14px;
  font-weight: 700;
  margin-bottom: 5px;
  margin-top: 5px;
  font-size: 16px;
  line-height: 1.31;
  color: #3e4141;
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
        title: 'APIN Health Initiative',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1598956040/timadoos/timadoos-3_sfbhlt.jpg',
        services: 'Internet Newtorking,security design',
      },
      {
        title: 'Benysta Micro financial bank',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1598837709/timadoos/timadoos-project1_aklzim.jpg',
        services:
          'Solar Panel Installation, Security risk management, security design',
      },
      {
        title: 'BIPC Group',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872405/timadoos/timadoos-project2_z7jog3.png',
        services: 'Security risk management, security design',
      },
      {
        title: ' Archtik Consultant',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1598836768/timadoos/timadoos-3_xdhhox.png',
        services:
          'CCTV Installation, Security risk management, security design',
      },
      {
        title: 'Salcorn concept limited',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872582/timadoos/project-3_wl8zzo.png',
        services:
          'Solar Panel Installation Security risk management, security design',
      },
    ],
  }),
}
</script>