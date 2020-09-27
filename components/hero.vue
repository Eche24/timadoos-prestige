<template>
<v-container fluid class="pb-0 pt-0">
  <v-layout row justify-center align-center wrap fill-height class="bg-color pa-5">
    <v-flex xs12 md11 sm11 lg11 class="overlay">
      <!-- <v-carousel hide-delimiters cycle :show-arrows="false">
      <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src">-->
      <v-row class="fill-height pa-7" align="center" justify="center">
        <v-col class="text-center white--text" cols="12" style="margin-top:10%;">
          <h1
            class="text-capitalize textover"
            style="font-size:2.5rem; font-family: 'Roboto', sans-serif;"
          >The Eagle-Eyed Protection.</h1>
          <h2
            class="textover"
            style=" font-family: 'Roboto', sans-serif; 
          margin-top: 0;margin-bottom: 30px;color: #fff;font-size: 18px;line-height: 1.89;font-weight: 600;"
          >Timadoos Prestige Limited is an independent security consultant having technical expertise in security.</h2>
          <div >
          <!-- <v-btn large > -->
          <a href="/contact" class="hero-contact" style="background-color: #fff;">
            <!-- <button> -->
            Contact us now
            <!-- </button> -->
            </a>
          <!-- </v-btn> -->
          </div>
        </v-col>
      </v-row>
      <!-- </v-carousel-item>
      </v-carousel>-->
    </v-flex>
  </v-layout>
</v-container>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          src:
            'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597886019/timadoos/m_s9eu8n.jpg',
        },
        {
          src:
            'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872405/timadoos/timadoos-project2_z7jog3.png',
        },
        {
          src:
            'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597872405/timadoos/timadoos-project2_z7jog3.png',
        },
      ],
      cycle: true,
    }
  },
}
</script>
<style scoped>
.overlay {
  opacity: 1;
  /* background: #2196f333; */
  background-image: url(https://assets-global.website-files.com/5b6df8bb681f89ec20b48f37/5b6df8bb681f896a10b48f58_background-map.png);
  background-position: 50% 0;
  background-size: cover;
  background-repeat: no-repeat;
  padding: 50px;
}
.textover {
  line-height: 1.5em;
  text-shadow: 2px 2px 2px #000;
}
.bg-color {
  /* background-position: 50% 0;
  background-size: cover;
  background-repeat: no-repeat; */
  /* background-image: linear-gradient(90deg,#003588,#003588 0,#338b96); */
  background-image: linear-gradient(98deg, #003588, #003588, #338b96),
    linear-gradient(180deg, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5));
}
.hero-contact {
  /* margin-top: 50px; */
  padding: 8px 25px;
  border-radius: 1px;
  -webkit-transition: all 0.2s ease;
  transition: all 0.2s ease;
  color: #6d6f6f;
  line-height: 30px;
  font-weight: 700;
  display: inline-block;
}
.hero-contact:hover {
  background-color: #2e589b !important;
  color: #fff;
}
</style>