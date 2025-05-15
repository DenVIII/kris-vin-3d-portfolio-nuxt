<template>
  <section class="gallery">
    <h2 class="header gallery__header">Некоторые из моих работ:</h2>
    <div class="wrapper">
      <Splide
        :options="{ rewind: true }"
        aria-label="My Favorite Images"
      >
        <SplideSlide
          v-for="(slide, i) in slides"
          :key="i"
        >
          <NuxtPicture
            :src="slide.imageSrc"
            :sizes="sizesConfig"
            :modifiers="{
              fit: 'cover',
              quality: 40,
              dpr: [1, 2],
            }"
            alt="Слайд"
            loading="lazy"
            class="gallery__slide"
          />
        </SplideSlide>
      </Splide>
    </div>
  </section>
</template>

<script>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import "@splidejs/vue-splide/css";

export default {
  name: "GallerySection",
  props: ["slides"],
  components: {
    Splide,
    SplideSlide,
  },
  data: () => ({
    sizesConfig: {
      // 100vw на всех экранах + кастомные брейкпоинты
      xs: "100vw",
      sm: "100vw",
      md: "100vw",
      lg: "900px",
      xl: "900px",
      xxl: "1200px",
    },
  }),
};
</script>

<style lang="scss">
@use "@/assets/scss/variables" as *;

.gallery {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  padding: 50px 0;
  background-color: $color-primary;
  &__header {
    text-align: center;
    margin-bottom: 50px;
  }
  .wrapper {
    width: 900px;
  }
  &__slide {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center center;
  }
}

.vueperslides {
  position: relative;
  &__arrow {
    color: $color-dark;
  }
  &__bullets {
    color: $color-dark;
  }
}

.splide__slide img {
  width: 100%;
  height: auto;
}

.splide__pagination {
  bottom: 1.5em;
}

@media (max-width: 1024px) {
  .gallery {
    min-height: auto;
    &__header {
      margin-bottom: 50px;
    }
    .wrapper {
      width: 100%;
    }
  }
}

@media (max-width: 800px) {
  .gallery {
    padding: 40px 0;
    &__header.header {
      padding: 20px 0;
    }
  }
}

@media (max-width: 500px) {
  .gallery {
    min-height: auto;
    padding: 0;
    &__header {
      margin-bottom: 0;
    }
  }
}
</style>
