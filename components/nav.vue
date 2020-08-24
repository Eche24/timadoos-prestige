<template>
  <nav>
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
        style="font-family: 'Montserrat', sans-serif; text-transform: uppercase; font-weight:600;"
      >follow us</span>
      <v-btn v-for="icon in icons" :key="icon" class="mx-4 black--text" icon :href="icon.src">
        <v-icon size="24px">{{ icon.icon }}</v-icon>
      </v-btn>
        </v-list-item-action>
      </v-list>
    </v-navigation-drawer>
    <v-card class="pt-4" flat>
      <v-layout row justify-center align-center wrap fill-height>
        <v-flex xs10 md11 sm11 lg11>
          <v-app-bar
            style="box-shadow:-21.213px 21.213px 30px 0px rgba(158, 158, 158, 0.3);"
            scroll-off-screen
            color="white"
            flat
          >
            <v-app-bar-nav-icon class="hidden-sm-and-up" @click.stop="drawer = !drawer" />
            <!-- <v-toolbar-title> -->
            <nuxt-link to="/">
              <img
                src="https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597845174/timadoos/Timadoos-01_pb9c9v.png"
                width="45vh"
              />
            </nuxt-link>
            <nuxt-link
              to="/"
              style="font-family: &quot;Tenali Ramakrishna&quot;, sans-serif; text-transform: capitalize;"
            >
              <span style="font-size:120%;">timadoos prestige</span>
            </nuxt-link>
            <!-- </v-toolbar-title> -->
            <!-- <v-spacer /> -->
            <v-btn-toggle color="blue" group v-model="toggle_exclusive" shaped class="ml-12">
              <v-btn
                text
                v-for="(item, i) in items"
                :key="i"
                :to="item.to"
                router
                exact
                class="hidden-xs-only"
                flat
              >
                <span
                  v-text="item.title"
                  color="#000"
                  style="font-family: 'Montserrat', sans-serif;text-transform: uppercase; font-weight:600;"
                ></span>
              </v-btn>
            </v-btn-toggle>
            <!-- </v-toolbar-items> -->
            <v-spacer />
            <v-card-actions class="hidden-xs-only">
              <span
                style="font-family: 'Montserrat', sans-serif; text-transform: uppercase; font-weight:600;"
              >follow us</span>
              <v-btn
                v-for="icon in icons"
                :key="icon"
                class="mx-4 black--text"
                icon
                :href="icon.src"
              >
                <v-icon size="24px">{{ icon.icon }}</v-icon>
              </v-btn>
            </v-card-actions>
          </v-app-bar>
        </v-flex>
      </v-layout>
    </v-card>
  </nav>
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
          src: '',
          icon: 'mdi-facebook',
        },
        {
          src: '',
          icon: 'mdi-twitter',
        },
        { src: '', icon: 'mdi-instagram' },
      ],
      title: ' ',
      toggle_exclusive: undefined,
    }
  },
}
</script>
