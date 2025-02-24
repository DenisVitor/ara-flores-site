<script setup lang="ts">
import AppFooter from "./src/components/footer/AppFooter.vue";
import AppHeader from "./src/components/header/AppHeader.vue";
import AppHome from "./src/components/main/AppHome.vue";
</script>
<style lang="css">
html,
body {
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
<template>
  <div>
    <AppHeader />
    <AppHome />
    <AppFooter />
  </div>
</template>
