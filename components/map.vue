<template>
  <v-container fluid class="contact-form-wrap pt-0 pb-0">
    <v-layout row wrap justify-center align-center fill-height>
      <v-flex xs10 md11 sm11 lg11>
        <v-row>
          <v-col cols="12" md="5" sm="8">
            <v-card class="pa-2 mx-auto" outlined tile>
              <v-card-text>
                <h1 class="contact-form-title">Contact Us</h1>
                <div class="text--primary">
                  <ul style="font-size:90%">
                    <li>
                      <v-icon color="grey" class="pr-2">mdi-phone</v-icon>+2347067289613, +2347016908497
                    </li>
                    <li>
                      <v-icon color="grey" class="pr-2">mdi-message-text</v-icon>contact@timadoosprestige.com
                    </li>
                    <li>
                      <v-icon color="grey" class="pr-2">mdi-map-marker</v-icon>No.81 JS Tarka way, Makurdi, Benue State,Nigeria
                    </li>
                  </ul>
                </div>
              </v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" md="7" sm="7">
            <v-card max-width="566" max-height="300" class="mx-auto map" outlined tile>
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1976.7735282299243!2d8.523007619788558!3d7.731646280930988!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1050804da4706407%3A0xd29a1b547818fbfd!2s81%20J%20S%20Tarka%20Road%2C%20Makurdi%2C%20Nigeria!5e0!3m2!1sen!2sus!4v1598604349479!5m2!1sen!2sus"
                width="600"
                height="450"
                frameborder="0"
                style="border:0;"
                allowfullscreen
                aria-hidden="false"
                tabindex="0"
              ></iframe>
            </v-card>
          </v-col>
        </v-row>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<style scoped>
.map{
    overflow:hidden;
    padding-bottom:56.25%;
    position:relative;
    height:0;
}
.map iframe{
    left:0;
    top:0;
    height:100%;
    width:100%;
    position:absolute;
}
li {
  list-style: circle;
  font-size: 14px;
  padding: 5px;
}
.contact-form-title {
  margin-top: 0;
  color: #3e4141;
  font-size: 24px;
  line-height: 1.3;
  margin-bottom: 10px;
  font-weight: 700;
}
.contact-form-wrap {
  padding-top: 50px;
  padding-bottom: 50px;
  background-color: #fcfcfc;
}
</style>