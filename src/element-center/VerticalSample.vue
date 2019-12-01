<template>
  <div>
    <h1>垂直居中</h1>
    <div style="border:2px solid green;height:400px">
      <div style="height:50px;border:1px solid red;">
        <label style="line-height:50px">单行文本label垂直居中：设置line-height为父级行高</label>
      </div>

      <div class="parent">
        <div class="son">垂直居中:after方式</div>
      </div>
      <div style="border:1px solid red;height:50px;position:relative;">
        <div
          style="border:1px solid red;height:30px;
        position:absolute;top:50%;transform:translateY(-50%); "
        >绝对定位垂直居中transform方式： position:absolute;top:50%;transform:translateY(-50%);</div>
      </div>

      <div style="border:1px solid red;height:50px;position:relative;">
        <div
          style="position:absolute;top:50%;height:20px;margin-top:-10px;color:red;"
        >绝对定位垂直居中margin-top:0.5*元素height</div>
      </div>
      <!-- 不可行 -->
      <!-- <div style="display;flex;align-items:center;height:50px;">
        <div>Flex 2012版。优点：内容块的高度任意，优雅的溢出。缺点：IE8/IE9不支持，需要浏览器前缀，渲染可能会有问题</div>
      </div>-->
      <br />
      <div style="border:1px solid red;height:50px;position:relative;">
        <div
          style="border:1px solid red;position:absolute;top:0;bottom:0;
        margin:auto 0;height:30px;"
        >绝对定位垂直居中:top：0;bottom:0;margin:auto 0;</div>
      </div>

      <!-- <div style="display:table;border:1px solid red;height:50px;">
        <div
          style="display:table-cell;vertical-align:middle;border:1px solid blue;"
        >父：display:table; 子：dispaly:table-cell;vertical-align:middle;</div>
      </div>-->
    </div>
    <!-- <div class="vertical1">垂直居中：margin:0 auto</div>
    <div class="vertical2">
      <div>垂直居中：flex布局 1</div>
      <br />
      <div>垂直居中：flex布局 2</div>
    </div>
    <div class="vertical3">垂直居中：table方法</div>
    <br />
    <div>垂直居中并据左右边距一定距离：</div>-->
  </div>
</template>

<script>
export default {
  name: "vertical-sample"
}
</script>

<style  scoped>
.parent {
  border: 2px solid blue;
  /* text-align: center; */ /*设置可水平居中*/
  height: 100px;
  /* overflow: hidden; */
}

.parent::after {
  content: "";
  display: inline-block;
  vertical-align: middle;
  height: 100%;
  /* left: 100px; */
  /* right:100px; */
}

.son {
  display: inline-block;
  vertical-align: middle;
  border: 1px solid blue;
  /* left:100px; */
  /* right: 100px; */
}
</style>