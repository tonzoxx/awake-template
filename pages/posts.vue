<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <main-section theme="one-column">
      <template>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="0" />
      </template>
    </main-section>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  }
}
</script>

<style>
.about-page .container {
  max-width: 560px;
  margin: auto;
}
</style>
