<template>
  <div class="logo-wrapper">
    <h2>Emily Miller</h2>
  </div>
</template>
<script>
export default {
  name: 'SiteLogo',
  data() {
    return {
      frames: 5,
      currentFrame: 1,
      blinking: true
    }
  },
  mounted() {
    setInterval(() => {
      const rand = Math.ceil(Math.random() * 10)
      this.blinking = rand % 2
    }, 1000)
  }
}
</script>
<style lang="scss">
@keyframes logoBlink {
  100% {
    transform: translateY(-360px);
  }
}
.logo-wrapper {
  position: relative;
  height: 50px;
  overflow: hidden;
  width: 200px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  font-size: 24px;
}
</style>
