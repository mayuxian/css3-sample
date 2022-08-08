<template>
  <!-- <MaskImage /> -->
  <Shuangfeiyi/>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import MaskImage from './animation/MaskImage.vue'
import Shuangfeiyi from './examples/shuangfeiyi-layout/index.vue'
export default defineComponent({
  name: 'App',
  components: {
    MaskImage,
    Shuangfeiyi
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>