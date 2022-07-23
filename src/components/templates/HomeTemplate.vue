<template>
  <section class="home-template">
    <HeaderProfile />
  </section>
</template>

<script setup>
import HeaderProfile from "../molecules/HeaderProfile.vue";
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.home-template {
  background: $bg;
  height: 100vh;
  width: 100%;
  padding: $s2;
  //   color: $yellow-1;
}
</style>
