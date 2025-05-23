<template>
  <section class="about">
    <h2 class="header about__header">Обо мне:</h2>
    <div class="wrapper">
      <div class="about__content">
        <p class="about__caption">
          Занимаюсь 3D-визуализацией жилых интерьеров. Разрабатываю композицию
          кадра и освещение, подбираю декор для передачи объема и атмосферы
          пространства.
        </p>
        <p class="about__caption">
          Со мной вы получите качественную визуализацию концепции в
          согласованном световом сценарии точно в срок. Если у вас есть вопросы
          или хотите обсудить проект, свяжитесь со мной — я всегда на связи.
        </p>
        <p class="about__caption">
          Использую следующие инструменты:
          <br />
          <b>3Ds Max / Corona Renderer / V-Ray / Adobe Photoshop</b>
        </p>
        <div class="icons">
          <NuxtImg
            src="/icons/3ds-Max.svg"
            alt="3Ds Max"
            class="icon"
            width="48"
            height="48"
          />
          <NuxtImg
            src="/icons/Chaos-Corona-01.svg"
            alt="Corona"
            class="icon"
            width="48"
            height="48"
          />
          <NuxtImg
            src="/icons/V-Ray.svg"
            alt="V-Ray"
            class="icon"
            width="48"
            height="48"
          />
          <NuxtImg
            src="/icons/Adobe-Photoshop.svg"
            alt="Photoshop"
            class="icon"
            width="48"
            height="48"
          />
        </div>
      </div>
      <NuxtPicture
        :sizes="sizesConfig"
        :modifiers="{
          fit: 'cover',
          quality: 80,
          dpr: [1, 2],
        }"
        :img-attrs="{ style: 'aspect-ratio: 3/2;' }"
        src="/img/close-up-1.jpg"
        alt="Пример работы: близкое изображение цветка перед загородным домом"
        loading="lazy"
        class="about__image"
      />
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutSection",
  data: () => ({
    sizesConfig: {
      xs: "90vw",
      sm: "90vw",
      md: "400px",
      lg: "600px",
      xl: "600px",
      xxl: "900px",
    },
  }),
};
</script>

<style lang="scss">
@use "@/assets/scss/variables" as *;

.about {
  min-height: 100vh;
  padding-bottom: 40px;
  .wrapper {
    position: relative;
    min-height: 500px;
  }
  &__header {
    text-align: center;
    padding: 40px 0;
  }
  &__content,
  &__image {
    transform: translateY(100px);
    transition:
      opacity 1s ease-in-out,
      transform 2s ease-in-out;
  }
  &__content {
    position: absolute;
    margin-top: 40px;
    left: 20%;
    display: flex;
    flex-direction: column;
    gap: 20px;
    justify-content: space-between;
    align-items: center;
    background-color: $color-primary;
    border-radius: 20px;
    width: 500px;
    height: 500px;
    padding: 40px;
  }
  &__caption {
    text-indent: 2ch;
    text-align: left;
    color: $color-dark;
    font-family: $font-family-text;
  }
  &__image {
    position: absolute;
    top: 0%;
    right: 10%;
    aspect-ratio: 2/3;
    border-radius: 20px;
    z-index: -1;
  }
}
.icons {
  display: flex;
  gap: 10px;
  .icon {
    border-radius: 8px;
  }
}

@media (max-width: 1024px) {
  .about {
    margin: 0 auto;
    width: 768px;
    min-height: auto;
    &__content {
      position: static;
    }
    &__image {
      top: -5%;
      right: -10%;
      width: 400px;
      height: 300px;
      border-radius: 10px;
      z-index: -1;
    }
  }
}

@media (max-width: 800px) {
  .about {
    margin: 0 auto;
    width: 100%;
    padding: 0 5vw;
    .wrapper {
      margin: 0 auto;
    }
    &__content {
      padding: 20px 30px;
      margin-top: 0;
      margin-bottom: 20px;
      width: 100%;
      height: auto;
    }
    &__image {
      position: static;
      width: 100%;
      height: auto;
    }
    &__caption:last-of-type {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .icons {
      margin-top: 10px;
    }
  }
}

@media (max-width: 500px) {
  .about {
    padding: 0 20px;
    min-height: auto;
    &__header {
      margin-bottom: 0;
    }
  }
}
</style>
