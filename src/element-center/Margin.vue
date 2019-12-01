<template>
  <div>
    <h2>margin合并问题</h2>
    <h3>设置margin-top,margin-bottom，则垂直方向取最大取值，不是累加，这属于margin垂直合并问题。</h3>
    <div>
      margin重叠合并的4种情况：
      <a href="https://blog.csdn.net/qq_30977953/article/details/90018402">Margin重叠问题</a>
      <ol>
        <li>父元素与第一个子元素之间</li>
        <li>父元素与最后一个子元素之间</li>
        <li>相邻的兄弟元素之间</li>
        <li>元素自身内部</li>
      </ol>
      <div class="father">
        <div class="box1"></div>
        <!-- <label>测试</label> -->
        <!-- 发生了塌陷 -->
        <div class="box2"></div>
      </div>
    </div>
    <h3>margin垂直合并解决方案：</h3>
    <ol>
      <li>安装最大值进行计算和设置</li>
      <li>通过display: inline-block;</li>
    </ol>
    <div>
      <ol>
        <li>设置某个最大的为期望的top值</li>
        <li>[只]设置兄弟中某一个元素：display:inline-block;都设置布局会错开</li>
      </ol>
    </div>
    <div style="height:3px;background:gray;margin:20px auto;"></div>
    <h2>margin塌陷问题</h2>
    <h3>设置子元素margin-top,margin-bottom，父元素会跟着子元素一起位移。</h3>
    <div>
      <div class="parent">
        <!-- 具有行内元素也可解决塌陷问题 -->
        <div class="child">嵌套父子，父塌陷</div>
      </div>
    </div>
    <h3>解决塌陷的方式：</h3>
    <div>
      <ol>
        <a href="https://www.jianshu.com/p/498145565e4f">使用BFC（Block Formatting Context)的方式。</a>
        <p>父级元素设置</p>
        <li>position:absolute/fixed</li>
        <li>border: 1px solid transparent;</li>
        <li>display: inline-block;</li>
        <li>display: table; (父元素会根据子元素进行自动扩大)</li>
        <li>overflow: hidden;(子元素被父元素切割)</li>
        <li>float: left;</li>
        <li>padding-top: 1px;</li>
        <li>具有行内元素也可解决塌陷问题</li>
      </ol>
    </div>
  </div>
</template>

<script>
export default {
  name: "margin"

}
</script>

<style   scoped>
/* * {
  padding: 0;
  margin: 0;
} */
.parent {
  background: yellow;
  height: 50px;
  width: 400px;
  /* border: 1px solid transparent; */
  /* position: absolute;*/ /* fixed */
  /* display: inline-block; */
  display: table; /*会根据子元素进行自动扩大*/
  /* float: left;  */ /*float:right;*/
  /* overflow: hidden; */ /*子元素被父元素切割*/
  /* padding-top: 1px; */
  /*具有行内元素也可解决塌陷问题*/
}
.child {
  background: green;
  height: 200px;
  width: 300px;
  margin-top: 20px;
}

.father {
  border: 1px solid red;
}
.box1 {
  width: 300px;
  height: 30px;
  background: pink;
  margin-bottom: 50px;
  /* display: inline-block; */
  /* border: 1px solid red; */
  /* overflow: hidden; */
  /* float: left; */
}
.box2 {
  /* display: inline-block;   */
  /* overflow: hidden; */
  width: 300px;
  height: 30px;
  background: blue;
  margin-top: 60px;
  /* border: 1px solid red; */
}
</style>