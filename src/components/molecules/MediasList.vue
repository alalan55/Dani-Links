<template>
  <div class="media-list">
    <ul>
      <li>
            <dl-button/>
      </li>
    </ul>
  </div>
</template>

<script setup>
import dlButton from '../atoms/dl-button.vue'

</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";
.media-list {

  padding: $s1 0;

  ul {
    padding: 0;

    li {
      list-style: none;
    }
  }
}
</style>
