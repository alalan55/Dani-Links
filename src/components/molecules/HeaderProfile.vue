<template>
  <header class="header">
    <figure>
      <div class="header__image"></div>
    </figure>
    <div class="header__profile">
      <span> @profile_user </span>
    </div>
  </header>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.header {
  width: 100%;
  padding: $s2 $s1;
  color: whtie;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: $s1;
  figure {
    background: white;

    width: 80px;
    height: 80px;
    border-radius: 50%;
  }
  &__profile {
    span {
      font-size: 1.25em;
      font-weight: 800;
      color: $yellow-1;
    }
  }
}
</style>
