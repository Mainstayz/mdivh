<template>
  <v-app id="inspire">
 <v-navigation-drawer
      v-model="drawer"
      app
    >
      <!--  -->
    </v-navigation-drawer>


    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-main>
      <v-container class="d-flex grey lighten-5" fluid>
    <v-row
      no-gutters
      style="flex-wrap: nowrap;"
    >
      <v-col
        cols="2"
        class="flex-grow-0 flex-shrink-0"
      >
        <v-card
          class="pa-2"
          outlined
          tile
        >
          I'm 2 column wide
        </v-card>
      </v-col>
      <v-col
        cols="1"
        style="min-width: 100px; max-width: 100%;"
        class="flex-grow-1 flex-shrink-0"
      >
        <v-card
          class="pa-2"
          outlined
          tile
        >
          I'm 1 column wide and I grow to take all the space
        </v-card>
      </v-col>
      <v-col
        cols="5"
        style="min-width: 100px;"
        class="flex-grow-0 flex-shrink-1"
      >
        <v-card
          class="pa-2"
          outlined
          tile
        >
          I'm 5 column wide and I shrink if there's not enough space
        </v-card>
      </v-col>
    </v-row>
  </v-container>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import HelloWorld from './components/HelloWorld.vue';

export default Vue.extend({
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
    drawer: null
  }),
});
</script>
