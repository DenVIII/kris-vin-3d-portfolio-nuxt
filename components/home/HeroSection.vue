<template>
  <section
    class="hero"
    id="hero"
    :style="`background-image: url(${bgUrl})`"
  >
    <div class="wrapper">
      <h1 class="hero__header header">3D Визуализатор</h1>
      <p class="hero__subheader">Кристина Виноградова</p>
      <p class="hero__subheader">"Визуализация ваших идей"</p>
    </div>
  </section>
</template>

<script setup>
const img = useImage();

const bgUrl = computed(() => {
  return img("/img/Library-day.Cam001F.jpg");
});
</script>

<style lang="scss">
@use "@/assets/scss/variables" as *;

.hero {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;

  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(31, 30, 30, 0.7);
    z-index: 1;
  }

  .wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
    z-index: 2;
  }
  &__header {
    color: $color-primary;
    font-size: 4rem;
    padding: 40px 0;
  }
  &__subheader {
    color: $color-primary;
    font-size: $font-size-subheaders;
    font-family: $font-family-text;
    font-weight: 300;
  }
}

@media (max-width: 600px) {
  .hero {
    background-attachment: scroll;
    &__header.header {
      font-size: 1.75rem;
    }
    &__subheader {
      font-size: 1rem;
    }
  }
}
</style>
