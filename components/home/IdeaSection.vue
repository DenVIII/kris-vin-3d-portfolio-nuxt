<template>
  <section class="idea">
    <h2 class="header idea__header">От идеи до реализации:</h2>
    <ImgComparisonSlider class="slider idea__slider">
      <!-- eslint-disable -->
      <NuxtPicture
        slot="first"
        src="/img/placeholder-1.jpg"
        :sizes="sizesConfig"
        :modifiers="{
          fit: 'cover',
          quality: 80,
          dpr: [1, 2],
        }"
        loading="lazy"
        class="slider__img first_img"
      />
      <NuxtPicture
        slot="second"
        src="/img/Modern-house-sunset.Cam012.jpg"
        :sizes="sizesConfig"
        :modifiers="{
          fit: 'cover',
          quality: 80,
          dpr: [1, 2],
        }"
        alt="Слайд"
        loading="lazy"
        class="slider__img second_img"
      />
      <!-- eslint-enable -->
    </ImgComparisonSlider>
  </section>
</template>

<script>
import { ImgComparisonSlider } from "@img-comparison-slider/vue";

export default {
  name: "IdeaSection",
  components: {
    ImgComparisonSlider,
  },
  data: () => ({
    sizesConfig: {
      // 100vw на всех экранах + кастомные брейкпоинты
      xs: "100vw",
      sm: "100vw",
      md: "100vw",
      lg: "100vw",
      xl: "100vw",
      xxl: "100vw",
    },
  }),
};
</script>

<style lang="scss">
@use "@/assets/scss/variables" as *;

.idea {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  &__header {
    padding: 40px 0;
  }
}

.slider {
  &__img {
    width: 100%;
  }
}

.slider:focus {
  outline: none;
}

@media (max-width: 1024px) {
  .idea {
    min-height: auto;
  }
}
</style>
