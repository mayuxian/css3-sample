<template>
  <h1>双飞翼布局</h1>
  https://www.cnblogs.com/jiguiyan/p/11425276.html
  <div id="center">
    <div id="inside">middle</div>
  </div>
  <div id="left">left</div>
  <div id="right">right</div>
</template>
      
<script>
//https://www.cnblogs.com/jiguiyan/p/11425276.html
export default {
  data() {
    return {}
  },
}
</script>
          
<style lang='stylus' scoped>
#center {
  float: left;
  width: 100%; /* 左栏上去到第一行 */
  height: 100px;
  background: blue;
}

#left {
  float: left;
  width: 180px;
  height: 100px;
  margin-left: -100%;
  background: #0c9;
}

#right {
  float: left;
  width: 200px;
  height: 100px;
  margin-left: -200px;
  background: #0c9;
}
//right 下面的样式也可以
// #right {
//   float: right;
//   width: 200px;
//   height: 100px;
//   margin-left: -100%;
//   background: #0c9;
// }

/* 给内部div添加margin，把内容放到中间栏，其实整个背景还是100% */
#inside {
  margin: 0 200px 0 180px;
  height: 100px;
}
</style>