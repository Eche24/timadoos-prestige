<template>
  <v-container fluid class="pa-0">
    <v-layout row wrap justify-center align-center fill-height class="footer-bg-color">
      <v-flex xs10 sm10 md10 lg10>
        <v-row>
          <v-col cols="12" sm="4" md="4" lg="4" class="text-center">
            <h3 style="font-size:110%" class="pb-3">Solutions</h3>

            <ul style="font-size:90%">
              <li>
                Call Center Solutions | Auto dialer | IP-PBX  
              </li>
              <li>
                Conference Solutions | IVRS |Voice Logger | Toll
              </li>
              <li>
                Free Handler Voice/SMS/Email Broadcasting
              </li>
            </ul>
          </v-col>

          <v-col cols="12" sm="4" md="4" lg="4" class="text-center">
            <h3 style="font-size:110%" class="pb-3">Contact Us</h3>
            <ul style="font-size:90%">
              <li>
                <v-icon color="grey">mdi-phone</v-icon> +2347067289623, +2347016908497
              </li>
              <li>
                <v-icon color="grey">mdi-message-text</v-icon> info@timadoosprestiga.com
              </li>
              <li>
                <v-icon color="grey">mdi-map-marker</v-icon>  No.81 JS Tarka way, Makurdi, Benue State,Nigeria
              </li>
            </ul>
          </v-col>

          <v-col cols="12" sm="4" md="4" lg="4">
            <!-- <v-list class="footer-bg-color text--white" > -->
            <h3 style="font-size:110%" class="pb-3 text-center text-xs-pt-2">Quick link</h3>
            <v-list-item
              v-for="(item, i) in items"
              :key="i"
              router
              exact
              class="text--white"
              dense
              :href="item.src"
            >
              <v-list-item-content class="text-white text-center">
                <v-list-item-title v-text="item.title" />
              </v-list-item-content>
            </v-list-item>
            <!-- </v-list> -->
          </v-col>
        </v-row>
        <!-- <v-divider color="white"></v-divider> -->
      </v-flex>
    </v-layout>
    <v-layout row wrap align-center justify-center class="copyright text-center">
      <v-flex xs10 sm10 md10 lg10>
        <span class style="font-size:100%">
          &copy; {{ new Date().getFullYear() }}
          <span style="color: #ff6000;">Timadoos Prestige Limited</span> All Rights
          Reserved
        </span>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
export default {
  data: () => ({
    icons: [
      {
        src: '',
        icon: 'mdi-facebook',
      },
      {
        src: '',
        icon: 'mdi-twitter',
      },
      { src: '', icon: 'mdi-instagram' },
    ],
    items: [
      // {
      //   title: 'Community',
      //   to: '/community',
      // },
      {
        title: 'Services',
        src: '/service',
      },
      {
        title: 'Projects',
        src: '/projects',
      },

      {
        title: 'about',
        src: '/about',
      },
    ],
  }),
}
</script>
<style scoped>
.footer-bg-color {
  background: #426186;
  color: #fff;
  line-height: 1.34em;
  letter-spacing: -0.01em;
  font-family: 'Montserrat', sans-serif;
}
.text-white {
  color: white;
  text-transform: capitalize;
}
li {
  list-style: none;
  padding-top: 10px;
  color: white;
}
h3 {
  border-bottom: 1px solid #fff;
  margin-bottom: 1.3em;
  padding-bottom: 1.3em;
  text-align: left;
  text-transform: uppercase;
  color: #fff;
  font-size: 1.4em;
  width: 100%;
}
.copyright {
  background: #eaeaea;
  -webkit-box-shadow: inset 0 20px 20px -20px rgba(0, 0, 0, 0.8);
  -moz-box-shadow: inset 0 20px 20px -20px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 20px 20px -20px rgba(0, 0, 0, 0.8);
  /* width: 100%; */
  padding: 1em 0;
}
</style>
