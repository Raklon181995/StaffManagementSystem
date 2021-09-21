<template>
  <div class="team">
    <h1>Team</h1>
    <v-cantainer class="my-5">
      <v-layout row warp>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card class="text-center ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="120px" class="grey lighten-2">
                <img :src="person.avatar" />
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn flat color="">
                <v-icon small left>mdi-message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-cantainer>
  </div>
</template>

<script>
export default {
  name: "Team",
  data() {
    return {
      team: [
        { name: "The Raklon", role: "Web developer", avatar: "./3.jpeg" },
        { name: "Riyo", role: "Web Designer", avatar: "./2.jpg" },
        { name: "Chun Li", role: "UX Designer", avatar: "./1.png" },
        { name: "The Ninja", role: "Java Developer", avatar: "./4.jpeg" },
        { name: "The Net Ninja", role: "UX Designer", avatar: "./5.jpeg" },
      ],
    };
  },
};
</script>
