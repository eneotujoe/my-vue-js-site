<template>
  <v-app>
 <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>John Leider</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>

        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      app
      color="primary"
      dark
    >
    <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="hidden-md-and-up"></v-app-bar-nav-icon>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-toolbar-item class="hidden-sm-and-down">
      <v-btn text>
        <span class="mr-2">Home</span>
      </v-btn>
      <v-btn text>
        <span class="mr-2">About</span>
      </v-btn>
      <v-btn text>
        <span class="mr-2">Contact</span>
      </v-btn>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
      </v-toolbar-item>

    </v-app-bar>

    <v-main>
      <v-container fluid>
      <HelloWorld/>
      </v-container>
    </v-main>
    <Footer/>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    HelloWorld,
    Footer,
  },

  data: () => ({
    drawer: null,
    items: [
            { title: 'Home', icon: 'mdi-view-dashboard' },
            { title: 'About', icon: 'mdi-help-box' },
          ],
  }),
};
</script>