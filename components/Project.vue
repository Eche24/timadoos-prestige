<template>
  <v-container fluid class="pa-0">
    <v-layout row justify-center align-center wrap fill-height class="pa-4 my-8">
      <v-flex xs10 md10 sm10 lg10>
        <h2>projects</h2>
        <v-row>
          <v-col cols="12" sm="6" md="6" v-for="card in cards" :key="card.title">
            <v-card class="pa-2 mx-auto" flat max-width="440">
              <v-img :src="card.src" height="200px"></v-img>
              <h4 class="pt-3">Client: {{card.title}}</h4>

              <P>
                <strong>Services:</strong> Security risk management, security design
              </P>
            </v-card>
          </v-col>
        </v-row>
        <span class="launch-wrap" style>
          <a href="/projects" target="_blank" rel="noopener noreferrer">View all our Projects</a>
        </span>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    cards: [
      {
        title: 'Archtik Group',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872014/timadoos/timadoos-project_b0sv3x.png',
      },
      {
        title: 'Benysta Micro financial bank',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872209/timadoos/timadoos-project1_iuq9ys.png',
      },
      {
        title: 'BIPC group',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872405/timadoos/timadoos-project2_z7jog3.png',
      },
      {
        title: 'Salcorn concept limited',
        src:
          'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872582/timadoos/project-3_wl8zzo.png',
      },
    ],
  }),
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
</style>