<template>
  <CardContainer />
</template>

<script lang="ts">
import Vue from 'vue';
import HelloWorld from '../components/HelloWorld.vue';
import CardContainer from '../components/CardContainer.vue';

export default Vue.extend({
  components: {
    CardContainer,
  },
});
</script>
