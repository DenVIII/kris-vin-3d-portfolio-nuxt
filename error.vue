<template>
  <section class="error-page">
    <h2 class="error-page__header">Упс, что-то пошло не так ;(</h2>
    <p class="error-page__text">
      Ошибка: <span class="error-page__code">{{ error.statusCode }}</span>
    </p>
    <NuxtLink
      to="/"
      class="error-page__ref"
      >Нажмите сюда, чтобы вернуться на главную.</NuxtLink
    >
  </section>
</template>

<script setup>
defineProps(["error"]);
</script>

<style lang="scss" scoped>
@use "@/assets/scss/variables" as *;
.error-page {
  padding: 10% 20%;
  height: 100vh;
  &__header {
    margin-bottom: 40px;
  }
  &__text {
    color: $color-dark;
    font-family: $font-family-text;
    margin-bottom: 20px;
  }
  &__ref {
    font-family: $font-family-text;
  }
  &__code {
    font-size: $font-size-subheaders;
    font-weight: bold;
  }
}
</style>
