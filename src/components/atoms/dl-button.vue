<template>
  <div class="button">
    <div class="button__title">
      <span> Título do botão </span>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";
.button {
  border: 2px solid $pink-1;
  padding: $s1;
  border-radius: 10px;
  transition: 0.2s ease-in;
  cursor: pointer;

  &__title {
    display: flex;
    align-items: center;
    justify-content: center;

    span {
      font-size: 1.1em;
      font-weight: 700;
      color: $pink-2;
      cursor: pointer;
    }
  }

  &:hover {
    background: $pink-1;

    .button__title {
      span {
        color: white;
      }
    }
  }
}
</style>
