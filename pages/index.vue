<template>
  <div id="home-page" class="page-wrapper home-page">
    <site-welcome
      :welcome-header="'Hi, I’m Emily 👋'"
      :welcome-message="
        'I’m a Digital Marketer Focusing on business intelligence based decision making via analyzing results of paid media, owned assets and digital campaigns to recommend adjustments and maximize revenue.'
      "
    ></site-welcome>

    <main-section theme="one-column">
      <template v-slot:default>
        <!-- All Posts -->
      </template>
      <template v-slot:sidebar>
        Nothing here
      </template>
    </main-section>
  </div>
</template>

<script>
import { mapState } from 'vuex'
import { setPageData } from '../helper'

export default {
  name: 'HomePage',
  head() {
    return {
      title: `Home | ${this.$siteConfig.siteName}`
    }
  },
  components: {},
  computed: {
    ...mapState(['title', 'subtitle', 'featureImage'])
  },
  fetch({ store, params }) {
    setPageData(store, { slug: 'home' })
  }
}
</script>

<style>
.home-page {
  margin-top: 66px;
}
.home-page .under-subtitle {
  border-top: none;
}
</style>
