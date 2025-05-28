<template>
  <div class="payment">
    <h2 class="payment__header payment__header_text">Оплата</h2>
    <section
      class="intro payment__intro"
      :style="`background-image: url(${bgUrl})`"
    >
      <h2 class="intro__header intro__header_title">Цена и условия оплаты</h2>
      <p class="intro__caption">
        Стоимость одного ракурса - от
        <span class="highlight">15 000 руб.</span><br /><br />Минимальное
        количество ракурсов в одном проекте -
        <span class="highlight">3 шт.</span><br /><br />Точную цену смогу
        назвать после изучения вашего технического задания.
      </p>
    </section>
    <section class="payment__details details">
      <h2 class="details__header">Подробнее:</h2>
      <ul class="details__list list">
        <h3 class="list__subheader subheader">Что входит в стоимость:</h3>
        <li class="list__item item">
          Создание 3D-модели здания с учетом архитектурных особенностей.
        </li>
        <li class="list__item item">
          Детальная проработка фасадов, материалов и окружающего ландшафта.
        </li>
        <li class="list__item item">
          Два круга правок:
          <ul class="list sub_list">
            <li class="list__item item sub_item">
              Первый — на этапе черновых рендеров (изменения в геометрии,
              материалах и освещении).
            </li>
            <li class="list__item item sub_item">
              Второй — после финальных рендеров.
            </li>
          </ul>
        </li>
        <li class="list__item item">
          Финальная постобработка изображений в Photoshop.
        </li>
      </ul>
      <ul class="details__list list">
        <h3 class="list__subheader subheader">Дополнительные условия:</h3>
        <li class="list__item item">
          <span class="highlight">3D-моделирование сложных элементов: </span>
          Декоративные элементы, уникальные конструкции обсуждаются отдельно.
        </li>
        <li class="list__item item">
          <span class="highlight">Техническое задание: </span>Необходимы чертежи
          (генплан, фасады, разрезы) и референсы по материалам.
        </li>
        <li class="list__item item">
          <span class="highlight">Срочные проекты: </span>Оплачиваются с
          наценкой от <span class="highlight">30%</span>.
        </li>
        <li class="list__item item">
          <span class="highlight">Ландшафтный дизайн: </span>Визуализация
          прилегающей территории рассчитывается отдельно.
        </li>
      </ul>
      <ul class="details__list list">
        <h3 class="list__subheader subheader">Типовые проекты:</h3>
        <li class="list__item item">
          Частные дома <span class="highlight">до 100 м²</span> -
          <span class="highlight">от 15 000 руб.</span> (3-5 ракурсов)
        </li>
        <li class="list__item item">
          Коттеджные поселки -
          <span class="highlight">от 50 000 руб.</span> (5-15 ракурсов)
        </li>
        <li class="list__item item">
          Жилые комплексы -
          <span class="highlight">от 40 000 руб.</span> за здание
        </li>
        <li class="list__item item">
          Генпланы территорий -
          <span class="highlight">от 10 000 руб.</span> за ракурс
        </li>
      </ul>
      <ul class="details__list list">
        <h3 class="list__subheader subheader">Условия оплаты:</h3>
        <li class="list__item item">
          Предоплата <span class="highlight">50%</span> для начала работы.
        </li>
        <li class="list__item item">
          Окончательный расчет после утверждения финальных визуализаций.
        </li>
        <li class="list__item item">
          Возможна поэтапная оплата для крупных проектов.
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
const img = useImage();

const bgUrl = computed(() => {
  return img("/img/Modern-house-day.Cam008.jpg");
});
</script>

<style lang="scss" scoped>
@use "@/assets/scss/variables" as *;

.highlight {
  font-weight: 600;
}

.payment {
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
  height: 90vh;
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
  &__caption {
    text-align: justify;
    z-index: 2;
    margin-top: 20px;
    width: 400px;
    padding: 20px 30px;
    border-radius: 20px;
    color: $color-dark;
    background-color: $color-primary;
    font-family: $font-family-text;
  }
}

.details {
  width: 960px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(3, auto);
  grid-column-gap: 30px;
  grid-row-gap: 20px;
  margin: 0 auto 40px auto;
  &__header {
    text-align: center;
    padding-top: 20px;
    grid-area: 1 / 1 / 2 / 3;
  }
}

.list {
  background-color: $color-primary;
  border-radius: 20px;
  padding: 20px 40px;
  &__item,
  &__subheader {
    margin-bottom: 10px;
    color: $color-dark;
  }
  &__subheader {
    font-family: $font-family-headers;
  }
  &__item {
    font-family: $font-family-text;
    list-style-type: disc;
  }
}

.sub_item {
  list-style-type: circle;
}

.sub_item:last-child {
  margin-bottom: 0;
}

@media (max-width: 820px) {
  .details {
    width: 500px;
    display: flex;
    flex-direction: column;
    align-items: center;
    &__list {
      width: 100%;
    }
  }
}

@media (max-width: 500px) {
  .payment {
    &__header {
      font-size: 1.5rem;
    }

    &__details {
      width: 100%;
    }
  }

  .intro {
    background-attachment: scroll;
    &__header {
      font-size: 1.5rem;
    }

    &__caption {
      width: 80%;
      height: auto;
      padding: 20px 30px;
    }
  }
  .details {
    &__header {
      font-size: 1.5rem;
    }
    &__list {
      border-radius: 0;
      padding: 20px 20px 20px 40px;
    }

    .sub_list {
      padding: 20px;
    }
  }
}
</style>
