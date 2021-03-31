<template>
  <div class="mask"></div>
</template>
      
<script>
export default {
  data() {
    return {}
  },
}
</script>
          
<style lang='scss' scoped>
@keyframes mask {
  0% {
    -webkit-mask-position: 0px 0px;
  }

  25% {
    -webkit-mask-position: 619px 0px;
  }

  50% {
    -webkit-mask-position: 0px 0px;
  }

  75% {
    -webkit-mask-position: 308px 0px;
    // -webkit-mask-position: 308px 0px;
    -webkit-mask-size: 100%;
  }

  100% {
    -webkit-mask-size: 1000%;
  }
}

.mask {
  width: 700px;
  height: 392px;
  position: relative;
  background: black url('./../assets/mask-background.jpg');
  -webkit-mask-image: url('./../assets/mask-image.jpg');
  // animation: mask 5s linear 1s 1 normal;
  animation: mask 5s linear 1s  infinite normal;
}
</style>