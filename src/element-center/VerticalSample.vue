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
      <div style="display:flex;align-items:center;height:50px;border:1px solid blue;">
        <div style="heigth:30px;border:1px solid red;">Flex垂直居中</div>
      </div>
      <br />

      <div style="border:1px solid red;height:50px;position:relative;">
        <div
          style="border:1px solid red;height:30px;
        position:absolute;top:50%;transform:translateY(-50%); "
        >绝对定位垂直居中：position:absolute;top:50%;transform:translateY(-50%);</div>
      </div>

      <div style="border:1px solid red;height:50px;position:relative;">
        <div
          style="position:absolute;top:50%;height:20px;margin-top:-10px;color:red;"
        >绝对定位垂直居中：position:absolute;top:50%;margin-top:0.5*元素height</div>
      </div>
      <div style="border:1px solid red;height:50px;position:relative;">
        <div
          style="border:1px solid red;position:absolute;top:0;bottom:0;
        margin:auto 0;height:30px;"
        >绝对定位垂直居中:position:absolute;top:0;bottom:0;margin:auto 0;</div>
      </div>
      <div style="display:table;border:1px solid pink;height:50px;">
        <div
          style="display:table-cell;vertical-align:middle;height:20px;background:gray;"
        >父：display:table; 子：dispaly:table-cell;vertical-align:middle;</div>TODO:table-cell的高度不起作用，有待研究
      </div>
    </div>
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
}

.parent::after {
  content: "";
  display: inline-block;
  vertical-align: middle;
  height: 100%;
}

.son {
  display: inline-block;
  vertical-align: middle;
  border: 1px solid blue;
}
</style>