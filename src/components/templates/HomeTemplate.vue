<template>
  <section class="home-template">
    <div class="home-template__content">
      <HeaderProfile />
      <MediaList :infos="list" />
    </div>
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
@import "@/assets/scss/mixins";

.home-template {
  background: $bg;
  min-height: 100vh;
  width: 100%;
  padding: $s2;
  transition: 0.2s ease-in;

  &__content {
    max-width: 1100px;
    margin: 0 auto;
  }

  @media (max-width: 600px) {
    @include dimension;
    &__content {
      @include dimensionChild;
    }
  }

  @media (min-width: 1400px) {
    @include dimension;
    &__content {
      @include dimensionChild;
    }
  }
}
</style>
