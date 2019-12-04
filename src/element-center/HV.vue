<template>
  <div>
    <h1>水平垂直居中</h1>
    <div class="hv_parent">
      <div class="hv_child1">
        方式一：盒模型?, left:0;right:0;top:0;bottom:0;margin:auto;
        <div>
          优点:简单
          缺点:没有足够空间时, 子元素会被截断, 但不会有滚动条.
        </div>
      </div>
    </div>
    <br />
    <div class="hv_parent">
      <div class="hv_child2">
        方式二：left: 50%;top: 50%;transform: translate(-50%, -50%);
        <div>
          优点:代码量少
          缺点:IE8不支持, 属性需要追加浏览器厂商前缀, 可能干扰其他 transform 效果, 某些情形下会出现文本或元素边界渲染模糊的现象.
        </div>
      </div>
    </div>
    <div class="hv_parent">
      <div class="hv_child3">
        方式三：height:固定;width:固定;left:50%;top:50%;margin-top:-0.5*height;margin-left:- 0.5*width;
        <div>
          优点:
          适用于所有浏览器.
          缺点:
          父元素空间不够时, 子元素可能不可见(当浏览器窗口缩小时,滚动条不出现时).如果子元素设置了overflow:auto, 则高度不够时, 会出现滚动条.
        </div>
      </div>
    </div>
    <h1>Flex布局</h1>
    <h2>Flex 优点：内容块的高度任意，优雅的溢出。缺点：IE8/IE9不支持，需要浏览器前缀，渲染可能会有问题</h2>
    <div class="hv_flex">
      <div style="width: 20px;">左</div>
      <div class="hv_flexChild">flex布局垂直水平居中</div>
      <div style="width: 20px;">右</div>
    </div>
    <br />flex布局中子元素中flex:x，x表示占比多少份。
    <div class="hv_flex">
      <div class="hv_flexChild1">红</div>
      <div class="hv_flexChild2">绿</div>
      <div class="hv_flexChild3">蓝</div>
    </div>
    <h1>after伪元素实现水平垂直居中</h1>
    <div class="parent">
        <div class="son">after伪元素实现水平垂直居中</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "hv-sample"
}
</script>

<style   scoped>
.hv_parent {
  position: relative;
  width: 600px;
  height: 180px;
  border: 1px solid red;
}

.hv_child1 {
  border: 2px solid green;
  position: absolute;
  /* height: 40px; */
  /* width: 400px; */
  left: 10px;
  right: 10px;
  top: 0;
  bottom: 0;
  margin: auto;
}

.hv_child2 {
  border: 2px solid blue;
  /* margin-left:50%; */
  /* margin-top: 50%; */
  width: 400px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

.hv_child3 {
  border: 2px solid green;
  position: absolute;
  height: 40px;
  width: 500px;
  left: 50%;
  top: 50%;
  margin-top: -20px;
  margin-left: -250px;
}

.hv_flex {
  display: flex;
  width: 600px;
  height: 100px;
  border: 1px solid red;
  justify-content: center;
  align-content: center;
  align-items: stretch; /*  stretch让盒子内的每个元素的高度都等于行高 */
}
.hv_flexChild {
  flex: 1;
  border: 2px solid green;
  left: 10px;
  right: 10px;
}

.hv_flexChild1 {
  flex: 1;
  border: 1px solid red;
  left: 10px;
  right: 10px;
  background: red;
}

.hv_flexChild2 {
  flex: 2;
  border: 1px solid green;
  left: 10px;
  right: 10px;
  background: green;
}
.hv_flexChild3 {
  flex: 3;
  border: 1px solid blue;
  left: 10px;
  right: 10px;
  background: blue;
}

.parent {
  border: 2px solid blue;
  text-align: center;
  height: 100px;
  width: 600px;
  /* overflow: hidden; */
}

.parent::after {
  content: "";
  display: inline-block;
  vertical-align: middle;
  height: 100%;
  /* width: 100%; */
}

.son {
  display: inline-block;
  vertical-align: middle;
  border: 1px solid red;
  /* width: 100%; */
}

.parent {
  border: 2px solid blue;
  text-align: center; /*设置可水平居中*/
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