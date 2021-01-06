<template>
  <div id="home-page" class="page-wrapper home-page">
    <site-welcome
      :welcome-header="'Hi, I’m Emily 👋'"
      :welcome-message="
        'I’m a Digital Marketer focusing on business intelligence based decision making via analyzing results of paid media, owned assets and digital campaigns to recommend adjustments and maximize revenue.'
      "
    ></site-welcome>

    <main-section theme="one-column">
      <template v-slot:default>
        <h6 class="subtitle is-4">
          A Few Of My Latest Posts
        </h6>
        <posts-grid :per-row="1" :number="3" />
        <div class="button-wrap">
          <nuxt-link to="/posts" class="round-centered-btn">
            All Posts
          </nuxt-link>
        </div>
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
.home-page .page-main-section {
  margin-top: 0px;
}
.home-page .under-subtitle {
  border-top: none;
}
.home-page .container {
  max-width: 560px;
}
.round-centered-btn {
  background-color: #3b80f0;
  padding: 10px 20px;
  border-radius: 11px;
  color: #fff;
  transition: 0.3s;
  display: inline-block;
}
a.round-centered-btn:hover {
  box-shadow: #000000a3 0px 10px 18px -10px;
  color: #fff;
}
.card {
  border-radius: 11px 11px 0px 0px;
  border-bottom: 1px #3b80f0 solid;
  transition: 0.3s;
}
.card:hover {
  box-shadow: #000000a3 0px 10px 18px -10px;
}
.image.is-2by1 {
  padding-top: 50%;
  border-radius: 11px 11px 0px 0px;
}
.button-wrap {
  display: block;
  text-align: center;
}
@media (max-width: 768px) {
  .header-block {
    width: calc(100% - 3.25rem);
  }
}
</style>
