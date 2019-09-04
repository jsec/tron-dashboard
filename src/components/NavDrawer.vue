<template>
  <v-navigation-drawer class="deep-purple accent-4" app clipped dark>
    <v-list>
      <v-list-item link>
        <v-list-item-icon>
          <v-icon>mdi-home</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title>Home</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-list-item link>
        <v-list-item-icon>
          <v-icon>mdi-volume-high</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title>Sounds</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';
@Component
export default class NavDrawer extends Vue {}
</script>
