<template>
  <nav class="navigation">
    <router-link to="/"> Home </router-link> |
    <router-link :to="{ name: 'About' }">About</router-link>|
    <router-link :to="{ name: 'Jobs' }">Jobs</router-link>
  </nav>
  <router-view />
</template>

<style lang="scss">
@import "assets/scss/style.scss"
</style>

//npx json-server --watch db.json (command to start 'json-server')