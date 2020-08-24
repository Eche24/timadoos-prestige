<template>
<v-layout row justify-center align-center wrap fill-height class="">
    <v-flex xs10 md11 sm11 lg11>
  <v-carousel hide-delimiters cycle :show-arrows="false">
    <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src">
      <v-row class="fill-height overlay hidden-xs-only" align="center" justify="center">
        <v-col class="text-center white--text pt-5" cols="12" style="margin-top:10%;">
          <!-- <h4
            class="textover"
            style=" font-family: 'Roboto', sans-serif; font-size:150%; font-weight: 900; font-style:italic"
          >IT/Security company</h4> -->
          <h1
            class="text-capitalize textover"
            style="font-size:3rem; font-family: 'roboto', sans-serif;"
          >timadoos prestige limited</h1>
        </v-col>
      </v-row>
    </v-carousel-item>
  </v-carousel>
    </v-flex>
</v-layout>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          src:
            "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597886019/timadoos/m_s9eu8n.jpg",
        },
        {
          src:
            "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597871647/timadoos/Inverter_P_H_20170810_180127_ksjvmd.jpg",
        }
      ],
      cycle: true,
    };
  },
};
</script>
<style scoped>
.overlay {
  /* opacity: 1;
      background: rgba(129, 199, 132, 0.47); */
}
.textover {
  line-height: 1.5em;
  text-shadow: 2px 2px 2px #000;
  
}
</style>