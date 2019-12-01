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
    <!-- <horizontal-sample></horizontal-sample> -->
    <!-- <vertical-sample></vertical-sample> -->
    <hv-sample></hv-sample>
    <!-- <margin></margin> -->
  </div>
</template>
<script>
// import HorizontalSample from './HorizontalSample';
// import VerticalSample from './VerticalSample';
import HvSample from './HV';
// import Margin from './Margin';
export default {
  name: "element-center-sample", 
  data() {
    return {}
  },
  components: {
    HvSample,
    // HorizontalSample,
    // VerticalSample,
    // Margin
  }
}
</script>

<style  scoped>
</style>