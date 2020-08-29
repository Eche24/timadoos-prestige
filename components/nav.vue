<template>
  <v-container fluid class="bg-color pt-4">
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" temporary app>
      <v-list dense nav>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact>
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
        <v-list-item-action>
          <span
            style="font-family: 'Montserrat', sans-serif; text-transform: uppercase; font-weight:700;"
          >follow us</span>
          <v-btn v-for="icon in icons" :key="icon" class="mx-4 black--text" icon :href="icon.src" target="blank">
            <v-icon size="24px">{{ icon.icon }}</v-icon>
          </v-btn>
        </v-list-item-action>
      </v-list>
    </v-navigation-drawer>
    <!-- <v-card class="pt-4" flat> -->
    <v-layout justify-center align-center fill-height class="overlay">
      <v-flex xs10 md11 sm11 lg11 class>
        <v-app-bar color="white" flat class="bg-color">
        <v-app-bar-nav-icon class="hidden-sm-and-up" @click.stop="drawer = !drawer" />
        <v-toolbar-title>
        <nuxt-link to="/">
          <img
            src="https://res.cloudinary.com/ds4yhjjq8/image/upload/v1598478347/timadoos/Timadoos-01_qdavwj.svg"
            width="70vh"
          />
        </nuxt-link>
        <!-- <nuxt-link
            to="/"
            style="font-family: &quot;Tenali Ramakrishna&quot;, sans-serif; text-transform: capitalize;"
          >
            <span style="font-size:120%;">timadoos prestige</span>
        </nuxt-link> -->
        </v-toolbar-title>
        <v-spacer />
        <v-btn-toggle group v-model="toggle_exclusive" shaped >
          <v-btn
            text
            v-for="(item, i) in items"
            :key="i"
            :to="item.to"
            class="hidden-xs-only"
            color="white"
            v-text="item.title"
            style="font-family: 'Montserrat', sans-serif;text-transform: uppercase; font-weight:700; opacity: 1 !important;"
          ></v-btn>
        </v-btn-toggle>
        <v-spacer />
        <span
          style="font-family: 'Montserrat', sans-serif; font-weight:700;"
          class="hidden-xs-only mr-3"
        >Follow Us</span>
        <v-btn v-for="icon in icons" :key="icon" class="hidden-xs-only" icon :href="icon.src">
          <v-divider vertical style="color:white"></v-divider>
          <v-icon size="24px" :style="{ 'color': icon.color}" class="mx-3">{{ icon.icon }}</v-icon>
        </v-btn>
        </v-app-bar>
      </v-flex>
    </v-layout>
    <!-- </v-card> -->
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      drawer: false,
      fixed: false,
      items: [
        // {
        //   icon: 'mdi-apps',
        //   title: 'Home',
        //   to: '/',
        // },
        {
          icon: 'mdi-view-dashboard',
          title: 'About',
          to: '/about',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Services',
          to: '/services',
        },
        {
          icon: 'mdi-dialpad',
          title: 'projects',
          to: '/projects',
        },
        {
          icon: 'mdi-dialpad',
          title: 'Contact',
          to: '/contact',
        },
      ],
      icons: [
        {
          src: 'https://www.facebook.com/Timadoos-Prestige-Ltd-440001943048064/?ref=page_internal',
          icon: 'mdi-facebook',
          color: 'white',
        },
        {
          src: '',
          icon: 'mdi-twitter',
          color: 'white',
        },
        { src: '', icon: 'mdi-instagram', color: 'white' },
      ],
      toggle_exclusive: undefined,
    }
  },
}
</script>
<style scoped>
.bg-color {
  /* background-position: 50% 0;
  background-size: contain;
  background-repeat: no-repeat; */
  background-image: linear-gradient(98deg, #003588, #003588, #338b96),
    linear-gradient(180deg, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5));
  color: #fff;
}
.overlay {
  /* background: #2196f333; */
  opacity: 1;
  background-image: url(https://assets-global.website-files.com/5b6df8bb681f89ec20b48f37/5b6df8bb681f896a10b48f58_background-map.png);
  background-position: 50% 0;
  background-size: contain;
  background-repeat: no-repeat;
  padding: 10px;
}
</style>