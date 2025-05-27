<template>
  <h2 class="portfolio__header">Мои работы:</h2>
  <project-slider
    v-for="(project, i) in projects"
    :key="i"
    :title="project.title"
    :description="project.description"
    :slides="project.slides"
    :verticalSlides="project.verticalSlides"
  ></project-slider>
</template>

<script>
import ProjectSlider from "@/components/portfolio/ProjectSlider.vue";
import ModernHouseImg1 from "/img/Modern-house-day.Cam008.jpg";
import ModernHouseImg2 from "/img/Modern-house-day-HDR.Cam009.jpg";
import ModernHouseImg3 from "/img/Modern-house-day-HDR.Cam004.jpg";
import ModernHouseImg4 from "/img/Modern-house-sunset.Cam012.jpg";
import ModernHouseImg5 from "/img/Modern-house-sunset.Cam007.jpg";
import ModernHouseImg6 from "/img/Modern-house-night.Cam006.jpg";
import LibraryImg1 from "/img/Library-day.Cam001F.jpg";
import LibraryImg2 from "/img/Library-day.Cam002.jpg";
import LibraryImg3 from "/img/Library-night.Cam004.jpg";
import LibraryImg4 from "/img/Library-sunset.Cam007.jpg";
import LibraryImg5 from "/img/Library-day.Cam005.jpg";
import ForestHouseImg1 from "/img/House-forest.Cam001.jpg";
import ForestHouseImg2 from "/img/House-forest.Cam002.jpg";
import ForestHouseImg3 from "/img/House-forest.Cam003.jpg";
import ForestHouseImg4 from "/img/House-forest.Cam004.jpg";
import ForestHouseImg5 from "/img/House-forest.Cam005.jpg";

export default {
  name: "PortfolioView",
  components: {
    ProjectSlider,
  },
  data: () => ({
    projects: [
      {
        title: "Загородный дом. ",
        description: "Проект загородного дома в стиле Лофт.",
        slides: [
          {
            id: "slide-1",
            imageSrc: ModernHouseImg1,
          },
          {
            id: "slide-2",
            imageSrc: ModernHouseImg2,
          },
          {
            id: "slide-3",
            imageSrc: ModernHouseImg3,
          },
          {
            id: "slide-4",
            imageSrc: ModernHouseImg4,
          },
          {
            id: "slide-5",
            imageSrc: ModernHouseImg5,
          },
          {
            id: "slide-6",
            imageSrc: ModernHouseImg6,
          },
        ],
        verticalSlides: false,
      },
      {
        title: 'Конкурсная работа: "Калифорнийская библиотека". ',
        description:
          "Проект библиотеки в г. Калифорния. Работа заняла 1-е место.",
        slides: [
          {
            id: "slide-1",
            imageSrc: LibraryImg1,
          },
          {
            id: "slide-2",
            imageSrc: LibraryImg2,
          },
          {
            id: "slide-3",
            imageSrc: LibraryImg3,
          },
        ],
        verticalSlides: [
          {
            id: "slide-4",
            imageSrc: LibraryImg4,
          },
          {
            id: "slide-5",
            imageSrc: LibraryImg5,
          },
        ],
      },
      {
        title: "Домик в лесу. ",
        description: "Концепт современного эко-жилища в хвойном лесу.",
        slides: [
          {
            id: "slide-1",
            imageSrc: ForestHouseImg1,
          },
          {
            id: "slide-2",
            imageSrc: ForestHouseImg2,
          },
          {
            id: "slide-3",
            imageSrc: ForestHouseImg3,
          },
          {
            id: "slide-4",
            imageSrc: ForestHouseImg4,
          },
          {
            id: "slide-5",
            imageSrc: ForestHouseImg5,
          },
        ],
        verticalSlides: false,
      },
    ],
  }),
};
</script>

<style lang="scss">
@use "@/assets/scss/variables" as *;

h1,
h2 {
  font-size: $font-size-headers;
  font-weight: $font-weight-headers;
  font-family: $font-family-headers;
}

h2,
p {
  color: $color-dark;
}
.portfolio__header {
  padding: 20px 0;
  text-align: center;
}
</style>
