<template>
  <nav
    class="navbar is-fixed-top"
    role="navigation"
    aria-label="main navigation"
  >
    <div class="navbar-constrain">
      <div class="navbar-brand">
        <nuxt-link class="navbar-item" to="/">
          <site-logo v-if="$siteConfig.logo === 'logo-component'" />
          <img
            v-else
            :src="$siteConfig.logo"
            :alt="$siteConfig.siteName"
            class="logo"
          />
        </nuxt-link>
      </div>

      <div
        :class="{
          'navbar-menu-custom': true,
          'is-active': active
        }"
      >
        <ul class="navbar-end-custom">
          <li
            v-for="item in $siteConfig.mainMenu"
            :key="item.link"
            class="navbar-item-custom"
            @click="active = false"
          >
            <component
              :is="item.link.startsWith('http') ? 'a' : 'nuxt-link'"
              :href="item.link"
              :to="item.link"
              :target="item.target ? item.target : '_self'"
            >
              {{ item.name }}
            </component>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  name: 'SiteNav',

  data() {
    return {
      active: false
    }
  }
}
</script>
<style lang="scss" scoped>
.navbar-item img {
  max-height: 2rem;
}
.navbar-burger {
  height: auto;
}
.navbar-constrain {
  display: flex;
  width: 650px;
  margin: auto;
  background-color: #fff;
}
.navbar-menu a {
  display: block;
  color: #4a4a4a;
}
.navbar-menu a:hover,
.navbar-brand a:hover {
  display: block;
  color: #3b80f0;
}

.navbar-menu-custom {
  display: flex;
  flex-grow: 1;
  flex-shrink: 0;
  justify-content: flex-end;
}
.navbar-end-custom {
  display: flex;
}
.navbar-item-custom {
  margin: 0 10px;
  padding: 15% 0;
  align-items: center;
}
.navbar-item-custom a {
  color: #4a4a4a;
}
.navbar-item-custom a:hover {
  color: #3b80f0;
}
@media screen and (max-width: 1023px) {
  .header-block {
    width: 420px;
}
  .navbar-menu-custom {
    flex-grow: 0.3;
  }
}
</style>
