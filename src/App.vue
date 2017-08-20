<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
};
</script>

<style lang="scss">
@import "~bulma/bulma.sass";

$fa-font-path: "~font-awesome/fonts";
@import "~font-awesome/scss/font-awesome";
</style>

