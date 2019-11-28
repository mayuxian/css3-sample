<template>
  <div id="app">
    <!--  测试
    使用flex布局，显示页面，展现列表。-->
    <element-center-sample></element-center-sample>
  </div>
</template>

<script>

import ElementCenterSample from './element-center/Sample';
export default {
  name: 'app',
  components: {
    ElementCenterSample
  }
}
</script>

<style>
#app {
}
</style>
