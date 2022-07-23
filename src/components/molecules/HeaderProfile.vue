<template>
  <header class="header">
    <figure>
      <img src="/img/profile-image.jpg" alt="Imagem de perfil" />
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
  padding: 0 $s1;
  color: whtie;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: $s1;
  figure {
    width: 85px;
    height: 85px;
    border-radius: 50%;
    overflow: hidden;
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
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
