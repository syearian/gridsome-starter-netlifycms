<template>
  <v-content>
    <slot/>
  </v-content>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
</style>
