<template>
  <v-app>
    <v-app-bar app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="headline text-uppercase">
        <span class="font-weight-light">TEAM </span>
        <span>TRON</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-navigation-drawer
      class="light-blue darken-4"
      app
      clipped
      dark
      v-model="drawer"
    >
      <v-list>
        <v-list-item router to="/">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item router to="/sounds">
          <v-list-item-icon>
            <v-icon>mdi-volume-high</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Sounds</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';
import CardContainer from './components/CardContainer.vue';

@Component({
  components: {CardContainer},
})
export default class App extends Vue {
  public name: string = 'App';
  public drawer = null;
}
</script>
