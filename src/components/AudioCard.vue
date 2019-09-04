<template>
  <v-card raised class="mx-auto" v-on:click="play">
    <v-card-title>{{ audio.name }}</v-card-title>
  </v-card>
</template>

<script lang="ts">
import {Component, Prop, Vue} from 'vue-property-decorator';
import {Audio} from '../interfaces/audio';

@Component
export default class AudioCard extends Vue {
  @Prop() private audio!: Audio;

  private play(): void {
    this.$http.get(`http://localhost:3000/audio/${this.audio.id}`);
  }
}
</script>
