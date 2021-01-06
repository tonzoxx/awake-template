<template>
  <div id="contact-page" class="page-wrapper contact-page content-page">
    <main-section theme="one-column">
      <template v-slot:default>
        <div class="button-wrap">
          <nuxt-link to="/posts" class="round-centered-btn linkedin">
            LinkedIn
          </nuxt-link>
          <nuxt-link to="/posts" class="round-centered-btn twitter">
            Twitter
          </nuxt-link>
        </div>
        <article class="tile is-child box">
          <p class="title">
            A Little About Me...
          </p>
          <figure class="image is-2by1 ">
            <opti-image
              :src="require('~/assets/uploads/contact-img.png').src"
              :srcset="require('~/assets/uploads/contact-img.png').srcSet"
            />
          </figure>
          <br />
          <div class="content">
            <p>
              <strong>
                Edit this page in<code>/pages/contact.vue</code>to fit your
                needs.
              </strong>
            </p>
            <p>
              “Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam, quis nostrud exercitation ullamco laboris
              nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
              reprehenderit in voluptate velit esse cillum dolore eu fugiat
              nulla pariatur. Excepteur sint occaecat cupidatat non proident,
              sunt in culpa qui officia deserunt mollit anim id est laborum.”
            </p>
            <p>
              “Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam, quis nostrud exercitation ullamco laboris
              nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
              reprehenderit in voluptate velit esse cillum dolore eu fugiat
              nulla pariatur. Excepteur sint occaecat cupidatat non proident,
              sunt in culpa qui officia deserunt mollit anim id est laborum.”
            </p>
          </div>
        </article>
      </template>
    </main-section>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: `Contact | ${this.$siteConfig.siteName}`
    }
  }
}
</script>
<style>
.contact-page .container {
  max-width: 560px;
}
</style>
