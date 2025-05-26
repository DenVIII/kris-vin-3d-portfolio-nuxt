<template>
  <section class="my-contacts">
    <h2 class="header my-contacts__header">Давайте поработаем вместе!</h2>
    <p class="subheader my-contacts__subheader">Мои контакты:</p>
    <div class="my-contacts__social social">
      <NuxtLink
        class="social__icon"
        to="#"
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
          src="/icons/Email_square.svg"
          alt="иконка Email"
          class="social__icon"
      /></NuxtLink>
      <NuxtLink to="#"
        ><img
          src="/icons/WhatsApp_square.svg"
          alt="иконка WhatsApp"
          class="social__icon"
      /></NuxtLink>
    </div>
  </section>
</template>

<style lang="scss">
@use "@/assets/scss/variables" as *;

.my-contacts {
  padding: 40px 0;
  padding-bottom: 80px;
  background-color: $color-primary;
  &__header {
    text-align: center;
    padding: 40px 0;
  }
  &__subheader {
    text-align: center;
    font-size: $font-size-subheaders;
    font-weight: 400;
  }
  &__social,
  &__subheader {
    transform: translateY(50px);
    font-family: $font-family-text;
    opacity: 0.5;
    transition:
      opacity 1s ease-in-out,
      transform 2s ease-in-out;
  }
}

.social {
  display: flex;
  justify-content: center;
  gap: 30px;
  padding: 20px 0;
  overflow: hidden;

  &__icon {
    width: 64px;
    height: 64px;
    border-radius: 10px;
    cursor: pointer;
    transition: all ease-in-out 500ms;
  }
  &__icon:hover {
    transform: translateY(-5px);
  }
}

@media (max-width: 500px) {
  .my-contacts {
    padding: 20px;
    &__subheader {
      font-size: 1.25rem;
    }
  }
  .social {
    gap: 15px;
    &__icon {
      width: 50px;
      height: 50px;
    }
  }
}
</style>
