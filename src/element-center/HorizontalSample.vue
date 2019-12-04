<template>
  <div>
    <!-- 内联块级元素：img、input -->
    <h1>水平居中</h1>
    <div style="text-align:center;">
      <label>行内元素label水平居中：父级style:"text-align:center"</label>
    </div>
    <div class="horizontal1">块级元素div居中：width固定 + margin:0 auto</div>
    <p class="horizontal3">块级元素居p水平居中：display:table;margin:0 auto</p>
    <li class="horizontal2">块级元素居li水平居中：display:flex;justify-content:center;</li>

    <div style="width:fit-content;margin:0 auto;">
      <div style="float:left;">水平居中:子元素float:left，父元素width:fit-content;margin:0 auto;</div>
    </div>
    <h3>绝对定位时，居中设置.为什么不是靠左?</h3>
    <div>
      <h3>绝对定位，居中设置</h3>
    </div>
    <div style="border:1px solid blue;height:50px;">
      <div
        style="position:absolute;left:50%;transform:translateX(-50%);border:1px solid red;height:50px;"
      >绝对定位水平居中：position:absolute;left:50%;transform:translateX(-50%);</div>
    </div>
    <div style="border:1px solid blue;height:50px;">
      <div
        style="position:absolute;left:0;right:0;width:400px;margin:0 auto;border:1px solid red;"
      >绝对定位水平居中：position:absolute;width:固定;margin:0 auto;left:0;right:0;</div>
    </div>
    <div style="border:1px solid blue;height:50px;">
      <div
        style="position:absolute;width:400px;left:50%;margin-left:-200px;border:1px solid blue;height:50px;"
      >绝对定位水平居中：position:absolute;width:固定;left:50%;margin-left:-0.5*宽度;</div>
    </div>
    <div style="border:1px solid blue;height:50px;">
      <div
        style="position:absolute;width:400px;left:50%;margin-left:-200px;border:1px solid blue;height:50px;"
      >绝对定位水平居中：position:absolute;width:固定;left:50%;margin-left:-0.5*宽度;</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "horizontal-sample"
}
</script>

<style  scoped>
/* fit-content   ?? */
.horizontal1 {
  height: 50px;
  width: 400px;
  margin: 0 auto;
  border: 1px solid red;
}
.horizontal2 {
  display: flex;
  justify-content: center;
  border: 1px solid red;
}
.horizontal3 {
  height: 50px;
  display: table;
  margin: 0 auto;
  border: 1px solid red;
}
</style>