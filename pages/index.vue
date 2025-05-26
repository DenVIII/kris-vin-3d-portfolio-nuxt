<template>
  <hero-section></hero-section>
  <gallery-section :slides></gallery-section>
  <about-section></about-section>
  <idea-section></idea-section>
  <my-contacts-section></my-contacts-section>
</template>

<script>
import AboutSection from "@/components/home/AboutSection.vue";
import GallerySection from "~/components/home/GallerySection.vue";
import HeroSection from "@/components/home/HeroSection.vue";
import IdeaSection from "@/components/home/IdeaSection.vue";
import MyContactsSection from "@/components/home/MyContactsSection.vue";

import image1 from "/img/Modern-house-day-HDR.Cam009.jpg";
import image2 from "/img/Modern-house-day.Cam008.jpg";
import image3 from "/img/Library-day.Cam002.jpg";
import image4 from "/img/Library-day.Cam001F.jpg";
import image5 from "/img/House-forest.Cam001.jpg";
import image6 from "/img/House-forest.Cam005.jpg";

export default {
  name: "HomeView",
  components: {
    HeroSection,
    GallerySection,
    AboutSection,
    IdeaSection,
    MyContactsSection,
  },
  data: () => ({
    slides: [
      {
        id: "slide-1",
        imageSrc: image1,
      },
      {
        id: "slide-2",
        imageSrc: image2,
      },
      {
        id: "slide-3",
        imageSrc: image3,
      },
      {
        id: "slide-4",
        imageSrc: image4,
      },
      {
        id: "slide-5",
        imageSrc: image5,
      },
      {
        id: "slide-6",
        imageSrc: image6,
      },
    ],
  }),
  mounted() {
    this.checkBlocksVisibility();
    window.addEventListener("scroll", this.checkBlocksVisibility);
  },
  methods: {
    checkBlocksVisibility() {
      // Добавляем блоки контента
      let blocks = [
        document.querySelector(".about__content"),
        document.querySelector(".about__image"),
        document.querySelector(".my-contacts__social"),
        document.querySelector(".my-contacts__subheader"),
      ];

      // Добавляем заголовки в основной массив
      const headers = document.querySelectorAll(".header");
      headers.forEach((header) => blocks.push(header));

      // Получаем высоту вьюпорта
      const windowHeight = window.innerHeight;

      // Добавляем стили к блокам
      blocks.forEach((block) => {
        const blockPosition = block.getBoundingClientRect().top;
        if (blockPosition < windowHeight - 100) {
          block.style.opacity = "1";
          block.style.transform = "translateY(0)";
        }
      });
    },
  },
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

.header {
  opacity: 0;
  transform: translateY(-50px);
  transition:
    opacity 1s ease-in-out,
    transform 1.5s ease-in-out;
}

@media (max-width: 800px) {
  .header {
    padding: 20px 0;
  }
}

@media (max-width: 500px) {
  h2,
  .header {
    font-size: 1.25rem;
  }
  p {
    font-size: 1rem;
  }
}
</style>
