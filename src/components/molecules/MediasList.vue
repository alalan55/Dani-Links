<template>
  <div class="media-list">
    <ul>
      <li v-for="item in props.infos" :key="item.id">
        <dl-button :button-data="item" />
      </li>
    </ul>
  </div>
</template>

<script setup>
import dlButton from "../atoms/dl-button.vue";

const props = defineProps({
  infos: { type: Array, required: true },
});
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";
.media-list {
  padding: $s1 0;

  ul {
    padding: 0;

    li {
      list-style: none;
      &:not(:last-child) {
        margin: $s1 0 $s2;
      }
    }
  }
}
</style>
