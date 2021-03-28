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
        dense
    >
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <v-btn text >
        新建测试用例
      </v-btn>
    </v-app-bar>
    <v-main>
      <div class="d-flex flex-column grey lighten-5" style="height: 100%">
        <v-row
            no-gutters
            style="flex-wrap: nowrap; height: 40%; background: beige"
        >
          <v-col
              cols="5"
              class="flex-grow-0 flex-shrink-0 yellow pa-2"
          >
          <v-item-group mandatory active-class="case-selected">
            <v-item v-slot="{active,toggle}">
              <v-card  @click="toggle">
                <v-card-title>这是一个标题</v-card-title>
                <v-card-subtitle>这是一个描述</v-card-subtitle>
                <v-card-actions>
                  <v-btn text>运行</v-btn>
                </v-card-actions>
              </v-card>
            </v-item>
            <v-item v-slot="{active,toggle}">
              <v-card  @click="toggle">
                <v-card-title>这是一个标题</v-card-title>
                <v-card-subtitle>这是一个描述</v-card-subtitle>
                <v-card-actions>
                  <v-btn text>运行</v-btn>
                </v-card-actions>
              </v-card>
            </v-item>
            <v-item v-slot="{active,toggle}">
              <v-card  @click="toggle">
                <v-card-title>这是一个标题</v-card-title>
                <v-card-subtitle>这是一个描述</v-card-subtitle>
                <v-card-actions>
                  <v-btn text>运行</v-btn>
                </v-card-actions>
              </v-card>
            </v-item>
          </v-item-group>

          </v-col>
          <v-col
              class="flex-grow-1 flex-shrink-0"
          >
            I'm 4 column widexxxx
          </v-col>
        </v-row>
        <v-row no-gutters>
          <v-col style="background: cadetblue">
            hello
          </v-col>
        </v-row>
      </div>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue'
import HelloWorld from './components/HelloWorld.vue'

export default Vue.extend({
  name: 'App',

  components: {
    HelloWorld
  },

  data: () => ({
    //
    drawer: null
  })
})
</script>
<style scoped>
.case-selected.v-card,.case-selected .v-card__subtitle{
  background-color: cadetblue !important;
  color: white !important;;
}

.case-selected .v-btn{
  color: white !important;;

}
</style>
