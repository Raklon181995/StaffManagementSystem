<template>
  <v-app class="grey lighten-4">
    <Navbar />

    <v-content class="mx-16">
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import Navbar from "@/components/Navbar";
import router from "./router/index";

export default {
  name: "App",
  components: { Navbar },
  router,

  data: () => ({
    //
  }),
};
</script>
