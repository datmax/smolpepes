<template>
  <v-app dark>
    <v-app-bar absolute app color="transparent" flat>
      <v-row align="center" justify="center">Smolpepes</v-row>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer absolute app color="transparent" class="py-6">
      <v-row align="center" justify="center">
        <span>
          <a href="https://twitter.com/smolpepes">
            <v-icon color="green">mdi-twitter</v-icon>
          </a>
        </span>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
    };
  },
};
</script>
<style>
* {
  font-family: "Press Start 2P", cursive;
}
</style>
