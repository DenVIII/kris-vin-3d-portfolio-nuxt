<template>
  <div class="contacts contacts__block">
    <section
      class="intro contacts__intro"
      :style="`background-image: url(${bgUrl})`"
    >
      <h2 class="intro__header intro__header_title">Мои контактные данные:</h2>
      <div class="intro__details">
        <h3 class="details__header">Мой электронный адрес:</h3>
        <NuxtLink
          to="#"
          class="details__email"
          >example@mail.ru</NuxtLink
        >
        <h3 class="details__header">И мои социальные сети:</h3>
        <div class="details__social">
          <NuxtLink to="#"
            ><img
              src="/icons/Telegram_square.svg"
              alt="иконка Telegram"
              class="social__icon"
          /></NuxtLink>
          <NuxtLink to="#"
            ><img
              src="/icons/VK_square.svg"
              alt="иконка вконтакте"
              class="social__icon"
          /></NuxtLink>
          <NuxtLink to="#"
            ><img
              src="/icons/WhatsApp_square.svg"
              alt="иконка WhatsApp"
              class="social__icon"
          /></NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const img = useImage();

const bgUrl = computed(() => {
  return img("/img/Modern-house-sunset.Cam012.jpg");
});
</script>

<style lang="scss" scoped>
@use "@/assets/scss/variables" as *;

.contacts {
  &__header {
    text-align: center;
    padding: 20px 0;
  }
}

.intro {
  position: relative;
  display: flex;
  flex-direction: column;
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
  &__header {
    color: $color-primary;
    z-index: 2;
  }
  &__details {
    z-index: 2;
    margin-top: 20px;
    width: 400px;
    padding: 30px 50px;
    border-radius: 20px;
    color: $color-dark;
    background-color: $color-primary;
    font-family: $font-family-text;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }
}

.details {
  &__email {
    font-size: 2rem;
    font-family: $font-family-headers;
    margin-bottom: 20px;
    color: $color-dark;
  }
  &__email:hover {
    cursor: pointer;
    font-weight: bold;
  }
}
.social__icon {
  margin: 10px;
}

@media (max-width: 820px) {
  .intro {
    background-position-x: 20%;
    padding: 20px 0;
    &__details {
      padding: 20px;
    }
  }
  .social {
    &__icon {
      width: 48px;
      height: 48px;
    }
  }
}

@media (max-width: 500px) {
  .intro {
    background-attachment: scroll;
    &__header {
      display: none;
    }
    &__details {
      width: 90%;
      padding: 20px;
    }
  }
  .details {
    &__email {
      font-size: 1.5rem;
      margin-bottom: 10px;
    }
  }
}
</style>
