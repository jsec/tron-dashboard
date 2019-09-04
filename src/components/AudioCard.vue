<template>
  <v-col cols="4">
    <v-card
      raised
      dark
      class="light-blue accent-4 audio-card"
      v-on:click="play"
    >
      <v-card-text>{{ audio.name }}</v-card-text>
    </v-card>
  </v-col>
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

<style scoped>
.audio-card {
  margin-top: 10px;
  margin-right: 10px;
  font-weight: bold;
}
</style>
