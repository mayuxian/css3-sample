<template>
  <div>
    <a href="https://www.cnblogs.com/yanqiu/p/8987126.html">HTML中块级元素和行内元素的总结和区分</a>
    <br />
    <a href="https://www.cnblogs.com/luoyishan/p/8316503.html">行内元素、内联元素、块级元素 详情1</a>
    <br />
    <a href="https://zhidao.baidu.com/question/381263705.html">行内元素、内联元素、块级元素 详情2</a>
    <br />
    <a href="https://blog.csdn.net/sinat_17775997/article/details/77547481">CSS盒子居中的几种方法</a>
    <!-- https://blog.csdn.net/weixin_42259266/article/details/89244691 -->
    <br />
    <!-- 内联块级元素：img、input -->
    <h1>水平居中</h1>
    <div style="text-align:center;">
      <label>行内元素label水平居中：父级style:"text-align:center"</label>
    </div>
    <div class="horizontal1">块级元素div居中：margin:0 auto</div>
    <!-- <div class="horizontal11">
      块级元素居li水平居中：display:flex;justify-content:center;margin:0 300px;
      <div class="margin:0 200px;border: 1px solid blue;">距离左右边距200px;</div>
    </div>-->
    <li class="horizontal2">块级元素居li水平居中：display:flex;justify-content:center;</li>
    <p class="horizontal3">块级元素居p水平居中：display:table;margin:0 auto</p>
    <div style="width:fit-content;margin:0 auto;">
      <div style="float:left;">水平居中:子元素float:left，父元素width:fit-content;margin:0 auto;</div>
    </div>
    <h3>绝对定位时，居中设置</h3>

    <!-- <div style="display:block;">
      <div
        style="position:absolute;left:50%;transform:translate(-50%,0);"
      >孩子居中：position:absolute;left:50%;transform:translate(-50%,0);</div>
    </div>-->
    <div
      style="position:absolute;left:0;right:0;width:400px;margin:0 auto;border:1px solid red;"
    >绝对定位居中</div>

    <!-- <div style="display:block;">
       TODO:   
      <div style="position:absolute;width:200px;left:50%;">孩子居中：</div>
    </div>-->
    <br />
    <h1>垂直居中</h1>
    <div style="border:2px solid green;height:600px">
      <div style="height:50px;border:1px solid red;">
        <label style="line-height:50px">单行文本label垂直居中：设置line-height为父级行高</label>
      </div>
      <div class="parent">
        <div class="son">垂直居中:after方式</div>
      </div>
      <div style="border:1px solid red;height:50px;position:relative;">
        <div style="position:absolute;top:50%;height:20px;margin-top:-10px;">垂直居中</div>
        <div style="position:absolute;left:50%;height:100%;border:1px solid blue;">水平居中据左右100px</div>
      </div>
        <div style="border:1px solid red;height:50px;position:relative;">
        <div style="position:absolute;height:20px;top:0;bottom:0;margin:auto 0;border:1px solid blue;">处置居中</div>
      </div>
      <!-- <div>
        <div class="parent1">垂直居中：绝对定位+height+top、bottom、margin</div>
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
  name: "element-center-sample",
  data() {
    return {}
  }
}
</script>

<style  scoped>
.parent2 {
  display: block;
}
.parent1 {
  position: absolute;
  height: 40px;
  top: 0;
  bottom: 0;
  margin: auto 0;
}
.parent {
  height: 50px;
  border: 1px solid red;
  text-align: center;
}
.parent::after {
  content: "";
  height: 100%;
}
.parent::after .son {
  display: inline-block;
  vertical-align: middle;
  height: 100%;
}

/* fit-content   ?? */
.horizontal1 {
  height: 100px;
  width: 100px;
  margin: 0 auto;
  border: 1px solid red;
}
.horizontal11 {
  display: flex;
  justify-content: center;
  border: 1px solid green;
}
.horizontal2 {
  display: flex;
  justify-content: center;
  border: 1px solid red;
}
.horizontal3 {
  display: table;
  margin: 0 auto;
  border: 1px solid red;
}
</style>