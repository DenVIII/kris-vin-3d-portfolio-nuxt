<template>
  <div class="conditions conditions__block">
    <h2 class="conditions__header conditions__header_text">Условия</h2>
    <section
      class="intro conditions__intro"
      :style="`background-image: url(${bgUrl})`"
    >
      <h2 class="intro__header intro__header_title">Визуализация интерьера</h2>
    </section>
    <section class="conditions__content conditions__content_wrapper">
      <div class="wrapper">
        <div class="benefits conditions__benefits">
          <h3 class="benefits__header">Что вы получите:</h3>
          <ul class="benefits__list list">
            <li class="list__item">
              <p class="item__title title">Фотореалистичные изображения</p>
              <p class="item__descr descr">
                Ваши идеи обретут жизнь с помощью детализированных
                3D-визуализаций. Каждый элемент интерьера будет выглядеть так,
                будто он уже существует в реальности.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Экономию времени и ресурсов</p>
              <p class="item__descr descr">
                Забудьте о бесконечных правках и пробных ремонтах. Вы сможете
                оценить и доработать дизайн до начала реальных работ, избежав
                лишних затрат.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Удобство и комфорт сотрудничества</p>
              <p class="item__descr descr">
                Я работаю с вами на каждом этапе, чтобы результат точно
                соответствовал вашим ожиданиям. Гибкий подход и оперативная
                обратная связь — мои приоритеты.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">
                Возможность экспериментировать без риска
              </p>
              <p class="item__descr descr">
                Используйте 3D-визуализацию, чтобы протестировать разные
                варианты отделки, мебели и освещения. Это безопасный способ
                убедиться, что выбранный дизайн идеально подходит для вашего
                пространства.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Легкость презентации проекта</p>
              <p class="item__descr descr">
                Создаю визуализации, которые помогут вам наглядно показать идею
                клиентам, заказчикам или подрядчикам. Это упрощает процесс
                согласования и вдохновляет всех участников проекта.
              </p>
            </li>
          </ul>
        </div>
        <div class="requirements conditions__requirements">
          <h3 class="requirements__header">Что от вас необходимо:</h3>
          <ul class="requirements__list list">
            <li class="list__item">
              <p class="item__title title">Планы помещения</p>
              <p class="item__descr descr">
                Чертежи с размерами: план расстановки мебели, план пола, план
                потолка и развертки стен (если есть декоративные элементы).
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Примеры отделочных материалов</p>
              <p class="item__descr descr">
                Фотографии или образцы текстур для стен, пола, потолка и других
                поверхностей.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Информация по мебели и декору</p>
              <p class="item__descr descr">
                Фотографии, ссылки на 3D-модели или артикулы мебели,
                светильников и декоративных элементов.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Стилистические предпочтения</p>
              <p class="item__descr descr">
                Примеры интерьеров, которые вас вдохновляют, или коллажи, чтобы
                передать настроение проекта.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Детализация по освещению</p>
              <p class="item__descr descr">
                Информация о расположении светильников, их типе и желаемой
                атмосфере освещения.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Особые пожелания</p>
              <p class="item__descr descr">
                Уточнения по декоративным элементам, молдингам, нишам или другим
                уникальным деталям.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Технические требования</p>
              <p class="item__descr descr">
                Если есть специфические пожелания по ракурсам, разрешению или
                формату визуализаций.
              </p>
            </li>
            <li class="list__item">
              <p class="item__title title">Обратная связь</p>
              <p class="item__descr descr">
                Готовность оперативно комментировать эскизы и вносить правки для
                достижения идеального результата.
              </p>
            </li>
          </ul>
        </div>
      </div>
      <div class="conditions__image"></div>
    </section>
    <section class="conditions__stages conditions__stages_wrapper">
      <h2>Этапы работы:</h2>
      <ul class="stages">
        <li class="stage">
          <div class="stage__number">1</div>
          <p class="stage__title title">Обсуждение и утверждение ТЗ</p>
          <p class="stage__descr descr">
            Вы присылаете техническое задание (планы, чертежи, примеры
            материалов и мебели). Мы обсуждаем детали, ракурсы и стилистику,
            чтобы я могла точно понять ваши ожидания. Вы вносите предоплату (50%
            от стоимости заказа) и я начинаю работу.
          </p>
        </li>
        <li class="stage">
          <div class="stage__number">2</div>
          <p class="stage__title title">Первое превью: геометрия и ракурсы</p>
          <p class="stage__descr descr">
            Я создаю базовую сцену с правильной геометрией и настраиваю ракурсы.
            Вы получаете черно-белый эскиз для утверждения композиции и внесения
            первых правок.
          </p>
        </li>
        <li class="stage">
          <div class="stage__number">3</div>
          <p class="stage__title title">Второе превью: материалы и текстуры</p>
          <p class="stage__descr descr">
            После согласования геометрии я добавляю материалы, текстуры и
            основное освещение. Вы оцениваете, как выглядит интерьер, и вносите
            корректировки по материалам и декору.
          </p>
        </li>
        <li class="stage">
          <div class="stage__number">4</div>
          <p class="stage__title title">
            Третье превью: детализация и финальные правки
          </p>
          <p class="stage__descr descr">
            Я добавляю детали: мебель, декор, светильники и другие элементы. Вы
            утверждаете финальный вид сцены, и мы вносим последние правки.
          </p>
        </li>
        <li class="stage">
          <div class="stage__number">5</div>
          <p class="stage__title title">Финальный рендер</p>
          <p class="stage__descr descr">
            После согласования всех деталей я выполняю финальный рендер в
            высоком разрешении. Вы вносите вторую часть платежа и получаете
            готовые изображения, которые точно передают, как будет выглядеть ваш
            интерьер.
          </p>
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
const img = useImage();

const bgUrl = computed(() => {
  return img("/img/3.jpg");
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
  height: 85vh;
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
    min-height: 1400px;
    padding-top: 40px;
    gap: 40px;
    margin: 0 auto;
    width: 960px;
    margin-bottom: 40px;
  }
  .wrapper {
    position: relative;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-column-gap: 40px;
    z-index: 2;
  }
  &__image {
    position: absolute;
    bottom: 0%;
    right: -5%;
    height: 420px;
    width: 960px;
    z-index: 1;
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

@media (max-width: 1000px) {
  .conditions {
    &__content {
      width: 800px;
    }
    &__image {
      width: 800px;
      right: 0%;
    }
  }
  .stages {
    width: 800px;
  }
}

@media (max-width: 800px) {
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
      position: static;

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
  }
  .conditions {
    &__content {
      padding: 20px 0;
    }
    &__image {
      display: none;
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
