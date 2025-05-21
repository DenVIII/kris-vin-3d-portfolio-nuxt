<template>
  <ClientOnly>
    <div class="project">
      <p class="project__caption">
        <span class="caption__title">{{ title }}</span>
        <span class="caption__descr">{{ description }}</span>
      </p>
      <div class="wrapper">
        <Splide
          :options="{ rewind: true }"
          aria-label="project"
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
                quality: 80,
                dpr: [1, 2],
              }"
              alt="Слайд"
              loading="lazy"
            />
          </SplideSlide>
        </Splide>
      </div>
      <div class="border"></div>
    </div>
  </ClientOnly>
</template>

<script>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import "@splidejs/vue-splide/css";

export default {
  name: "ProjectSlider",
  props: ["title", "description", "slides"],
  components: {
    Splide,
    SplideSlide,
  },
  data: () => ({
    sizesConfig: {
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

.project {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 50px;
  &__caption {
    font-family: $font-family-text;
    margin-bottom: 30px;
  }
  .wrapper {
    width: 900px;
  }
  .caption {
    &__title {
      font-weight: bold;
    }
  }
}

.border {
  margin-top: 40px;
  width: 50%;
  height: 4px;
  border-radius: 100%;
  background-color: #b8b4b433;
}

.vueperslides {
  &__arrow {
    color: $color-dark;
  }
  &__bullet:hover,
  &__bullet:focus,
  &__arrow:hover {
    color: $color-accent;
  }
}

@media (max-width: 1024px) {
  .project {
    .wrapper {
      width: 100%;
    }
  }
}

@media (max-width: 500px) {
  .portfolio__header {
    font-size: 1.5rem;
  }
  .project {
    padding: 20px 0;
    &__caption {
      text-align: center;
    }
  }
}
</style>
