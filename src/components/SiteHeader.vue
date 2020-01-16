<template>
  <v-app-bar app color="primary" dark>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
    <v-toolbar-title>
      <g-link to="/" class="white--text">{{ $static.metadata.siteName }}</g-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <nav class="d-flex justify-center">
      <g-link
        v-for="link in links"
        :key="link.href"
        :to="link.href"
        class="px-4 py-4 white--text"
      >
        {{ link.text }}
      </g-link>
    </nav>
  </v-app-bar>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  data: () => ({
    links: [
      {href: '/', text: 'Home'},
      {href: '/about', text: 'About Us'},
      {href: '/services', text: 'Services'},
      {href: '/contact', text: 'Contact Us'}
    ],
  })
}
</script>

<style>

</style>