<template>
  <section class="not-found">
    <h2 class="not-found__header">Упс, что-то пошло не так ;(</h2>
    <p class="not-found__text">Страница по этому адресу не найдена...</p>
    <a
      href="/"
      class="not-found__ref"
      >Нажмите сюда, чтобы перейти на главную.</a
    >
  </section>
</template>
<script>
export default {
  name: "PageNotFound",
};
</script>

<style lang="scss">
@use "@/assets/scss/variables" as *;
.not-found {
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
}
</style>
