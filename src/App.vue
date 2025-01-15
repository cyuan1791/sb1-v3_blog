<template>
  <!-- use vue3 and bootstrap 4 to create a blogpost. The post data is read from a json file. The main page display the title, data, author, image, summary and a read more link to read the content
  -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
      <router-link class="navbar-brand" to="/">Blog</router-link>
    </div>
  </nav>
  <router-view></router-view>
</template>

<style>
#app {
  text-align: left;
  max-width: none;
  padding: 0;
  margin: 0;
}
</style>
