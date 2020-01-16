<template>
  <v-footer
    color="primary"
    padless
  >
    <div class="d flex flex-column align-center">
      <nav class="d-flex justify-center">
        <g-link
          v-for="link in links"
          :key="link.href"
          :to="link.href"
          class="px-4 py-5 white--text"
        >
          {{ link.text }}
        </g-link>
      </nav>
      <div
        class=" d-flex justify-center primary darken-1 py-3 white--text body-2"
      >
        &copy; {{ new Date().getFullYear() }} &mdash; Vuetify
      </div>
    </div>
  </v-footer>
</template>

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