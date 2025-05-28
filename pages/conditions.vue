<template>
  <div class="conditions conditions__block">
    <h2 class="conditions__header conditions__header_text">Условия</h2>
    <section
      class="intro conditions__intro"
      :style="`background-image: url(${bgUrl})`"
    >
      <h2 class="intro__header intro__header_title">
        Визуализация экстерьеров
      </h2>
    </section>
    <section class="conditions__content conditions__content_wrapper">
      <div class="wrapper">
        <div class="benefits conditions__benefits">
          <h3 class="benefits__header">Что вы получите:</h3>
          <ul class="benefits__list list">
            <li class="list__item">
              <p class="item__title title">Фотореалистичные изображения</p>
              <p class="item__descr descr">
                Точное представление вашего объекта в реальных условиях с
                правильной передачей материалов, освещения и окружения.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Экономию времени и средств</p>
              <p class="item__descr descr">
                Возможность оценить и скорректировать дизайн до начала
                строительства, избежав дорогостоящих изменений на этапе
                реализации.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Профессиональный подход</p>
              <p class="item__descr descr">
                Работаю с вами на всех этапах, чтобы результат полностью
                соответствовал ожиданиям. Гибкость и оперативность - мои
                приоритеты.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Тестирование концепций</p>
              <p class="item__descr descr">
                Возможность сравнить разные варианты отделки фасадов,
                ландшафтного дизайна и освещения без финансовых рисков.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Эффективную презентацию</p>
              <p class="item__descr descr">
                Качественные визуализации помогут наглядно представить проект
                инвесторам, заказчикам или согласующим органам.
              </p>
            </li>
          </ul>
        </div>
        <div class="requirements conditions__requirements">
          <h3 class="requirements__header">Что от вас необходимо:</h3>
          <ul class="requirements__list list">
            <li class="list__item">
              <p class="item__title title">Генплан местности</p>
              <p class="item__descr descr">
                Для отображения прилегающей территории и окружающей застройки
                (если требуется).
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Архитектурные чертежи</p>
              <p class="item__descr descr">
                Поэтажные планы, фасады, разрезы и план кровли с указанием всех
                размеров.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Материалы отделки</p>
              <p class="item__descr descr">
                Фотографии или описания материалов фасада, кровли и других
                элементов экстерьера.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Стилистические референсы</p>
              <p class="item__descr descr">
                Примеры архитектурных объектов, которые вас вдохновляют, для
                понимания стиля проекта.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Освещение и окружение</p>
              <p class="item__descr descr">
                Пожелания по времени суток для визуализации и особенности
                ландшафтного дизайна.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Технические требования</p>
              <p class="item__descr descr">
                Предпочтения по ракурсам, разрешению и формату итоговых
                изображений.
              </p>
            </li>
          </ul>
        </div>
      </div>
      <div
        class="conditions__image"
        :style="`background-image: url(${bgUrl})`"
      ></div>
    </section>
    <section class="conditions__stages conditions__stages_wrapper">
      <h2>Этапы работы:</h2>
      <ul class="stages">
        <li class="stage">
          <div class="stage__number">1</div>
          <p class="stage__title title">Обсуждение проекта</p>
          <p class="stage__descr descr">
            Вы присылаете чертежи и техническое задание. Мы согласовываем
            ключевые ракурсы и детализацию. После внесения предоплаты (50%)
            начинается работа.
          </p>
        </li>
        <li class="stage">
          <div class="stage__number">2</div>
          <p class="stage__title title">Базовое моделирование</p>
          <p class="stage__descr descr">
            Создаю 3D-каркас здания и окружающего пространства. Вы получаете
            схематичные скетчи для утверждения композиции.
          </p>
        </li>
        <li class="stage">
          <div class="stage__number">3</div>
          <p class="stage__title title">Детализация фасадов</p>
          <p class="stage__descr descr">
            Добавляю материалы, текстуры и основное освещение. Предоставляю
            промежуточные рендеры для согласования.
          </p>
        </li>
        <li class="stage">
          <div class="stage__number">4</div>
          <p class="stage__title title">Ландшафт и окружение</p>
          <p class="stage__descr descr">
            Прорабатываю детали ландшафтного дизайна, растительность и
            окружающую среду. Вы утверждаете финальный вид.
          </p>
        </li>
        <li class="stage">
          <div class="stage__number">5</div>
          <p class="stage__title title">Финальная визуализация</p>
          <p class="stage__descr descr">
            После полной оплаты вы получаете высококачественные рендеры в
            выбранных ракурсах с постобработкой.
          </p>
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
const img = useImage();

const bgUrl = computed(() => {
  return img("/img/House-forest.Cam005.jpg");
});
</script>

<style lang="scss" scoped>
@use "@/assets/scss/variables" as *;

h1,
h2 {
  font-size: $font-size-headers;
  font-weight: $font-weight-headers;
  font-family: $font-family-headers;
  text-align: center;
}

h2,
p {
  color: $color-dark;
}

.intro {
  position: relative;
  display: flex;
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
}

.conditions {
  &__header {
    padding: 20px 0;
    text-align: center;
  }
  &__content {
    position: relative;
    padding-top: 40px;
    gap: 40px;
    margin: 0 auto;
    width: 960px;
    margin-bottom: 40px;
  }
  &__benefits,
  &__requierments {
    min-height: 100%;
    display: flex;
    flex-direction: column;
  }
  .wrapper {
    position: relative;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-column-gap: 40px;
    z-index: 2;
  }
  &__image {
    background-size: 175%;
    background-position: center;
    margin-top: 50px;
    margin-left: 80px;
    height: 420px;
    width: 960px;
  }

  h3 {
    font-family: $font-family-headers;
    color: $color-dark;
    text-align: center;
    margin-bottom: 20px;
  }
  p {
    font-family: $font-family-text;
    color: $color-dark;
  }
}

.list {
  background-color: $color-primary;
  border-radius: 20px;
  padding: 20px 40px;
  flex: 1;
  &__item {
    padding: 20px 0;
  }
  .title {
    font-weight: bold;
    margin-bottom: 10px;
  }
  .descr {
    text-align: left;
  }
}

.stages {
  display: grid;
  grid-template-rows: repeat(3, 1fr);
  grid-template-columns: repeat(2, 1fr);
  grid-column-gap: 40px;
  grid-row-gap: 60px;
  width: 960px;
  margin: 40px auto;
}

.stage {
  &__number {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.5rem;
    font-family: $font-family-headers;
    font-weight: $font-weight-headers;
    color: $color-dark;
    background-color: $color-primary;
    width: 50px;
    height: 50px;
    border-radius: 25px;
    margin-bottom: 15px;
  }
  &__title {
    display: flex;
    justify-content: start;
    gap: 30px;
    align-items: end;
    font-weight: bold;
    margin-bottom: 15px;
  }
}

.stage:nth-child(odd) {
  border-right: 3px dotted $color-primary;
  margin-right: -10px;
  padding-right: 10px;
}

@media (max-width: 1024px) {
  .conditions {
    &__content {
      width: 800px;
    }
    &__image {
      width: 800px;
      margin-left: 0;
    }
  }
  .stages {
    width: 800px;
  }
}

@media (max-width: 820px) {
  .conditions {
    .wrapper {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 20px;
    }
    &__content {
      width: 100%;
      padding: 20px 40px;
      margin-bottom: 20px;
    }
    &__image {
      margin-top: 20px;
      width: 100%;
    }
  }
  .stages {
    padding: 20px 40px;
    width: 100%;
    gap: 30px;
    margin-top: 20px;
  }
  .list {
    padding: 10px 20px;
    &__item {
      padding: 5px 0;
    }
  }
}

@media (max-width: 500px) {
  .intro {
    background-attachment: scroll;
    background-position-x: 30%;
  }
  .conditions {
    &__content {
      padding: 20px 0;
      padding-bottom: 0;
    }
    &__image {
      height: 150px;
      width: calc(100% - 20px);
      margin: 0 auto;
      margin-top: 20px;
    }
  }
  .list {
    border-radius: 0;
  }
  .stages {
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .stage:nth-child(odd) {
    border-right: none;
    margin-right: 0;
    padding-right: 0;
  }
  .stage {
    border-left: 3px dotted $color-primary;
    padding-left: 10px;
    margin-left: -10px;
  }
}
</style>
