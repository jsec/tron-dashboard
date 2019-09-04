<template>
  <v-container>
    <v-flex xs12>
      <AudioCard v-for="audio in audios" :audio="audio" v-bind:key="audio.id" />
    </v-flex>
  </v-container>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';
import {AxiosResponse} from 'axios';
import AudioCard from './AudioCard.vue';
import {Audio} from '../interfaces/audio';

@Component({
  components: {AudioCard},
})
export default class CardContainer extends Vue {
  private audios: Audio[] = [];

  private created(): void {
    this.$http
      .get('http://localhost:3000/audio')
      .then((response: AxiosResponse) => {
        this.audios = response.data.audios;
      });
  }
}
</script>
