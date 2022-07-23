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
  background: rgb(2, 0, 36);
  background: linear-gradient(
    99deg,
    rgba(2, 0, 36, 1) 0%,
    rgba(161, 0, 53, 1.5) 0%,
    rgba(255, 134, 158, 0.9948354341736695) 160%
  );
  min-height: 100vh;
  width: 100%;
  padding: $s2;
  transition: 0.2s ease-in;
  position: rela;

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
