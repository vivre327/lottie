<template>
<div>hi</div>
 <div id="lottie-container"></div>
</template>

<script>
export default {
  name: 'IntroAni',
  mounted() {
    try {
      window.lottie.loadAnimation({
        container: document.getElementById('lottie-container'),
        renderer: 'svg',
        loop: true,
        autoplay: true,
        path: require('@/assets/sample.json')
      });
    } catch (error) {
      console.error('Lottie 로딩 중 오류 발생:', error);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
#lottie-container {
  width: 500px;
  height: 500px;
  background-color: #ffff00;
}

</style>
