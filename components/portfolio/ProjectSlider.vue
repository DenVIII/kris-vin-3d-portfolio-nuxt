<template>
  <ClientOnly>
    <div class="project">
      <p class="project__caption">
        <span class="caption__title">{{ title }}</span>
        <span class="caption__descr">{{ description }}</span>
      </p>
      <div class="wrapper">
        <Splide
          :options="options"
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
              class="project__slide"
            />
          </SplideSlide>
        </Splide>
        <div
          class="wrapper vertical-slider"
          v-if="verticalSlides"
        >
          <Splide :options="{ rewind: true, autoHeight: true }">
            <SplideSlide
              v-for="(slide, i) in verticalSlides"
              :key="i"
            >
              <NuxtPicture
                :src="slide.imageSrc"
                :modifiers="{
                  fit: 'cover',
                  quality: 80,
                  dpr: [1, 2],
                }"
                alt="Слайд"
                loading="lazy"
                class="project__slide"
              />
            </SplideSlide>
          </Splide>
        </div>
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
  props: ["title", "description", "slides", "verticalSlides"],
  components: {
    Splide,
    SplideSlide,
  },
  data: () => ({
    sizesConfig: {
      xs: "100vw",
      sm: "100vw",
      md: "100vw",
      lg: "1100px",
      xl: "1100px",
      xxl: "1400px",
    },
    sizesConfigVertical: {
      xs: "100px",
      sm: "200px",
      md: "300px",
      lg: "600px",
      xl: "600px",
      xxl: "800px",
    },
    options: {
      autoWidth: true,
      rewind: true,
      type: "loop",
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
    text-align: center;
    padding: 0 20px;
    margin-bottom: 30px;
  }
  &__slide img {
    aspect-ratio: 16/9;
    object-fit: cover;
  }
  .wrapper {
    width: 1100px;
  }
}
.caption {
  &__title {
    font-weight: bold;
  }
}

.wrapper.vertical-slider {
  margin: 0 auto;
  margin-top: 40px;
  width: 600px;
  .project__slide img {
    aspect-ratio: 9/16;
  }
  .splide {
    &__slide {
      position: relative;
      aspect-ratio: 9/16;
      overflow: hidden;
    }
    &__slide img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
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

.splide {
  &__slide {
    position: relative;
    aspect-ratio: 16/9;
    overflow: hidden;
  }
  &__slide img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }
}

@media (max-width: 1024px) {
  .project {
    .wrapper {
      width: 100%;
    }
  }
  .wrapper.vertical-slider {
    width: 600px;
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
  .wrapper.vertical-slider {
    width: 300px;
  }
}
</style>
