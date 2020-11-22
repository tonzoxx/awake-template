<template>
  <div class="header-block">
    <h1>{{ welcomeHeader }}</h1>
    <p>{{ welcomeMessage }}</p>
  </div>
</template>

<script>
export default {
  name: 'SiteWelcome',
  props: {
    welcomeHeader: {
      type: String,
      default: 'test'
    },
    welcomeMessage: {
      type: String,
      defualt: 'test'
    }
  }
}
</script>
<style>
.header-block {
  width: 560px;
  margin: 0 auto;
  padding: 55px 0;
}
.header-block h1 {
  font-size: 22px;
  margin: 0 0 25px 0;
  text-align: center;
}
</style>
