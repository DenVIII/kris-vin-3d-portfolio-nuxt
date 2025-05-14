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
          <img
            :src="slide.imageSrc"
            :alt="`Слайд №${key}`"
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
    .wrapper {
      width: 100%;
    }
  }
}

@media (max-width: 800px) {
  .gallery {
    padding: 40px 0;
    &__header.header {
      padding: 0;
      margin-bottom: 40px;
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
