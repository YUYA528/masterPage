<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <Drawers />
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer">
      </v-app-bar-nav-icon>

      <v-toolbar-title>Hi</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <v-container app>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Drawers from "../components/Drawers.vue";
  export default {
    data: () => ({ drawer: false }),
    components: { Drawers }
}
</script>