<template>
  <h1>圣杯布局</h1>
  https://www.cnblogs.com/jiguiyan/p/11425276.html
  <div id="bd">
    <div id="middle">middle</div>
    <div id="left">left</div>
    <div id="right">right</div>
  </div>
</template>
      
<script>
export default {
  data() {
    return {}
  },
}
</script>
          
<style lang='stylus' scoped>
#bd {
  padding: 0 200px 0 180px;
  height: 100px;
}

#middle {
  float: left;
  width: 100%;
  height: 500px;
  background: blue;
}

#left {
  float: left;
  width: 180px;
  height: 500px;
  margin-left: -100%;
  background: #0c9;
  position: relative;
  left: -180px;
}

#right {
  float: left;
  width: 200px;
  height: 500px;
  margin-left: -200px;
  background: #0c9;
  position: relative;
  right: -200px;
}
</style>