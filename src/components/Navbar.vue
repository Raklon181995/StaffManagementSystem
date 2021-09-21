<template>
  <div>
    <nav>
      <v-toolbar flat>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title class="text-uppercase grey--text">
          <span class="font-weight-light">Todo</span>
          <span>Ninja</span>
        </v-toolbar-title>
        <v-spacer></v-spacer>

        <v-btn depressed color="white">
          <span>Sing Out</span>
          <v-icon right>mdi-export</v-icon>
        </v-btn>
      </v-toolbar>
      <v-navigation-drawer app v-model="drawer" absolute bottom temporary>
        <v-layout column align-center>
          <v-flex class="mt-5">
            <v-avatar size="120px">
              <img src="/3.jpeg" />
            </v-avatar>
            <p class="text-center subheading mt-1">
              The Raklon
            </p>
          </v-flex>
          <v-flex class="mt-4 mb-4">
            <Popup />
          </v-flex>
        </v-layout>
        <v-list>
          <v-list-item-group
            v-model="group"
            active-class="deep-purple--text text--accent-4"
          >
            <v-list-item to="/">
              <v-list-item-title>Dashboard</v-list-item-title>
            </v-list-item>
            <v-list-item to="project">
              <v-list-item-title>My project</v-list-item-title>
            </v-list-item>
            <v-list-item to="team">
              <v-list-item-title>Team</v-list-item-title>
            </v-list-item>
            <!-- <v-list
              v-for="link in links"
              :key="link.text"
              router
              :to="link.route"
            >
              <v-list-item>
                <v-list-item-title>{{ link.text }}</v-list-item-title>
              </v-list-item>
            </v-list> -->
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </nav>
  </div>
</template>

<script>
import Popup from "./Popup.vue";
export default {
  components: {
    Popup,
  },
  data() {
    return {
      drawer: false,
      links: [
        { text: "Dashboard", route: "/" },
        { text: "My Projects", route: "/project" },
        { text: "Team", route: "/team" },
      ],
    };
  },
};
</script>

<style></style>
