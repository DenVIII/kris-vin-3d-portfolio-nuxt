<template>
  <footer>
    <div class="row">
      <div class="logo row__column">
        <NuxtLink :to="{ path: '/', hash: '#hero' }">Kristy V.</NuxtLink>
      </div>
      <div class="socials row__column">
        <NuxtLink to="#"
          ><img
            src="/icons/Telegram_footer.svg"
            alt="иконка Telegram"
            class="socials__icon"
        /></NuxtLink>
        <NuxtLink to="#"
          ><img
            src="/icons/VK_footer.svg"
            alt="иконка вконтакте"
            class="socials__icon"
        /></NuxtLink>
        <NuxtLink to="#"
          ><img
            src="/icons/Email_footer.svg"
            alt="иконка Email"
            class="socials__icon"
        /></NuxtLink>
        <NuxtLink to="#"
          ><img
            src="/icons/WhatsApp_footer.svg"
            alt="иконка WhatsApp"
            class="socials__icon"
        /></NuxtLink>
      </div>
    </div>
    <div class="row">
      <p class="copyright row__column">Кристина Виноградова © 2025</p>
      <div class="menu row__column">
        <NuxtLink
          class="menu__item"
          :to="{ path: '/', hash: '#hero' }"
          >Главная</NuxtLink
        >
        <NuxtLink
          class="menu__item"
          to="/portfolio"
          >Портфолио</NuxtLink
        >
        <NuxtLink
          class="menu__item"
          to="/conditions"
          >Условия</NuxtLink
        >
        <NuxtLink
          class="menu__item"
          to="/payment"
          >Оплата</NuxtLink
        >
        <NuxtLink
          class="menu__item"
          to="/contacts"
          >Контакты</NuxtLink
        >
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
@use "@/assets/scss/variables" as *;

footer {
  background-color: $color-primary;
  padding: 40px 250px;
  box-shadow: 0 10px 10px 10px #18181833;
  .logo {
    font-family: $font-family-headers;
    font-weight: $font-weight-headers;
  }
}

footer a,
footer p {
  color: $color-dark;
}

.row {
  display: flex;
  justify-content: space-between;
  &__column {
    padding: 20px 0;
    display: flex;
    gap: 10px;
  }
}

.socials {
  &__icon {
    width: 30px;
    height: 30px;
  }
}

.menu {
  &__item {
    font-family: $font-family-text;
  }
}

.copyright {
  color: #636363;
  font-family: $font-family-text;
}

@media (max-width: 1024px) {
  footer {
    padding: 40px 80px;
  }
}

@media (max-width: 820px) {
  footer {
    padding: 20px 40px;
  }
}

@media (max-width: 500px) {
  footer {
    padding: 20px;
    .row {
      flex-direction: column-reverse;
      &__column {
        flex-wrap: wrap;
      }
    }
  }
}
</style>
