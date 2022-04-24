<template>
  <div>
  
  <comp2></comp2><comp></comp>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import comp from './components/comp.vue';
import comp2 from './components/comp2.vue';

export default defineComponent({
  name: 'App',
  components: {
    comp, comp2
  }
});
</script>

<style>

</style>
