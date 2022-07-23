<template>
  <div class="button" @click="go">
    <div class="button__title">
      <span> {{ props.buttonData.title }} </span>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  buttonData: { type: Object, required: true, default: null },
});

const go = () => {
  window.open(props.buttonData.path, "_blank");
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";
.button {
  border: 3px solid $pink-1;
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
      overflow-wrap: break-word;
      word-break: break-word;
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
