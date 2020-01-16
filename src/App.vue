<template>
  <v-app>
    <site-header />
    <router-view />
    <site-footer />
  </v-app>
</template>

<static-query>
query {
  metadata {
    siteName
    siteDescription
  }
}
</static-query>

<script>
import SiteHeader from '@/components/SiteHeader.vue'
import SiteFooter from '@/components/SiteFooter.vue'

export default {
  components: {
    SiteHeader,
    SiteFooter
  },
  metaInfo() {
    return {
      title: this.$static.metadata.siteName,
      meta: [
        {
          key: 'description',
          name: 'description',
          content: this.$static.metadata.siteDescription
        }
      ]
    }
  }
}
</script>

<style lang="scss">
a {
  text-decoration: none;

  &:hover,
  &:focus {
    text-decoration: underline;
  }
}
</style>
