<template>
  <section class="home-template">
    <HeaderProfile  />
    <MediaList :infos="list" />
  </section>
</template>

<script setup>
import { ref } from "vue";
import HeaderProfile from "../molecules/HeaderProfile.vue";
import MediaList from "../molecules/MediasList.vue";
import { infos } from "@/mock";

const list = ref([]);
list.value = infos;
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
