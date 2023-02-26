<template>
  <nav>
    <router-link to="/"> Home </router-link> |
    <router-link :to="{ name: 'About' }">About</router-link>
  </nav>
  <router-view />
</template>

<style lang="scss">
@import "assets/scss/style.scss"

</style>
