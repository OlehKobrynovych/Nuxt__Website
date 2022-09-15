<template>
    <div class="our-services" id="services">
        <h4 class="our-services__title">Послуги</h4>

        <!-- <div class="our-services__slider">
            <p>Створення сайту</p>
            <p>SEO оптимізація</p>
            <p>Доопрацювання сайту</p>
        </div> -->

        <div class="our-services--wrap container" >
            <figure
                class="our-services__card"
                v-for="servises in servises"
                :key="servises.id"
            >
                <img
                    src="https://images.pexels.com/photos/1173777/pexels-photo-1173777.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260"
                    alt="img24"
                />
                <figcaption class="our-services__card-caption">
                    <div class="our-services__card-caption-content">
                        <h2 class="our-services__card-caption-title">{{servises.title}}</h2>
                        <div class="our-services__card-caption-text-wrapper">
                            <p>{{servises.text}}</p>
                            <p>{{servises.prise}}</p>
                        </div>
                    </div>
                </figcaption>
            </figure>
        </div>

    </div>
</template>

<script>

export default {

  data() {
      return {
        //   isOpen: false,
        servises: [
            {id: 1, title: 'Сайт-візитка', text: 'Невеликий односторінковий сайт. Включає головний екран, блок з інформацією про вас (або вашої діяльності, послуги), блок з фото, блок з контактними даними. Максимальне заповнення сайту до 5 блоків, з формою зворотного звязку.', prise: 'Ціна: ****'},
            {id: 2, title: 'Лендінг', text: 'Сайт для бізнесу чи експерта описує товар чи послугу, їх переваги та необхідність купити. Мета сайту, щоб користувач здійснив цільову дію. Сайт містить форму збору даних, можливість підключити платіжні системи.', prise: 'Ціна: ****'},
            {id: 3, title: 'Корпоративний сайт', text: 'Багатосторінковий сайт для бізнесу, де зібрано та структуровано всю необхідну інформацію. Сайт має фірмовий стиль, містить контактні дані та форму зворотного звязку. Розповідає про діяльність компанії та її основні напрямки.', prise: 'Ціна: ****'},
            {id: 4, title: 'SEO оптимізація', text: 'Пошукова оптимізація та всебічний розвиток сайту в пошукових системах з метою отримання ТОП позицій та додаткових користувачів з органічної видачі (SERP). Якісне просування сайту у лідери тематики у пошуковій видачі.', prise: 'Ціна: ****'},
            {id: 5, title: 'Інтернет магазин', text: 'Сайт з каталогом товарів, їх опис та характеристикою. Вибраним, кошиком, доступними способами доставки оплати. Зручна навігація по товарах. Підключу CRM або оповіщення про замовлення товарів, можливість підключення адмін-панелі.', prise: 'Ціна: ****'},
            {id: 6, title: 'Доопрацювання сайту', text: 'Впроваджуємо нові "хотілки", розвиваємо функціонал, оптимізуємо роботу модулів і плагінів.', prise: 'Ціна: ****'},
        ],
      }
  },
  methods: {
    //   onOpen() {
    //       this.isOpen = !this.isOpen; 
    //   }
  },
}
</script>

<style scoped>
.our-services {

}

.our-services--wrap {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
}

.our-services__title {
    text-align: center;
    font-size: 22px;
    margin-top: 30px;
    margin-bottom: 20px;
}

/* ------- анімація появи тексту-------------- */

/* 
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #FFCC00;
}
@keyframes cursor {
  from, to {
    border-color: transparent;
  }
  50% {
    border-color: black;
  }
}
@keyframes typing {
  from {
    width: 100%;
  }
  90%, to {
    width: 0;
  }
}
@keyframes slide {
  33.3333333333% {
    font-size: 3rem;
    letter-spacing: 3px;
  }
  to {
    font-size: 0;
    letter-spacing: 0;
  }
}
.our-services__slider {
  font-family: Consolas, monospace;
  font-weight: bold;
  text-align: center;
  white-space: nowrap;
}
.our-services__slider p {
  position: relative;
  display: inline;
  font-size: 0;
  text-transform: uppercase;
  letter-spacing: 0;
  animation: slide 15s step-start infinite;
}
.our-services__slider p::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  border-left: 3px solid black;
  background-color: #fff;
  animation: typing 5s infinite, cursor 1s infinite;
}
.our-services__slider p:nth-child(1) {
  animation-delay: 0s;
}
.our-services__slider p:nth-child(1)::after {
  animation-delay: 0s;
  animation-timing-function: steps(16), step-end;
}
.our-services__slider p:nth-child(2) {
  animation-delay: 5s;
}
.our-services__slider p:nth-child(2)::after {
  animation-delay: 5s;
  animation-timing-function: steps(23), step-end;
}
.our-services__slider p:nth-child(3) {
  animation-delay: 10s;
}
.our-services__slider p:nth-child(3)::after {
  animation-delay: 10s;
  animation-timing-function: steps(12), step-end;
} */

/* ---------------------------- */
.our-services__card {
    position: relative;
    overflow: hidden;
    background: #3085a3;
    text-align: left;
    height: 350px;
    width: 30%;
    min-width: 240px;
    margin: 0;
    border-radius: 21px;
    box-shadow: 0 2px 1px 1px rgb(0 0 0 / 9%), 0 5px 4px 1px rgb(0 0 0 / 15%), 0 7px 10px -3px rgb(0 0 0 / 17%), 0 10px 13px -4px rgb(0 0 0 / 23%), 0 16px 20px -4px rgb(0 0 0 / 36%);
}

.our-services__card > img {
  width: 100%;
  height: 100%;
  -o-object-fit: cover;
  object-fit: cover;
  display: block;
  transition: transform 0.35s;
  transform: translate3d(0, 0, 0);
  will-change: transform;
}

.our-services__card:hover > img {
  transform: scale(1.15) translate3d(0, -20px, 0);
}

.our-services__card-caption {
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  display: flex;
  justify-content: center;
  background-color: rgba(23, 28, 47, 0.6);
  transition: all 0.3s;
  transform: translate3d(0, 100%, 0);
  will-change: transform;
}

.our-services__card-caption-content {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  width: auto;
  transition: all 0.3s;
  transform: translate3d(0);
  will-change: transform;
}

.our-services__card-caption-title {
  display: block;
  color: #fff;
  margin: 0;
  padding: 1.5rem;
  transition: all 0.3s;
  background-color: rgba(23, 28, 47, 0.4);
  transform: translate3d(0, -100%, 0);
  will-change: transform;
}

.our-services__card-caption p {
  padding: 0 1rem;
  margin-bottom: 10px;
  color: #fff;
  opacity: 0;
  transition: opacity 0.35s 0.1s;
  transform: translate3d(0);
  will-change: transform;
}

.our-services__card:hover > .our-services__card-caption {
  transform: translateY(0);
}

.our-services__card:hover > .our-services__card-caption > .our-services__card-caption-content {
  top: 23%;
  transform: translate(0, -9%);
}

.our-services__card:hover > .our-services__card-caption-title {
  background-color: rgba(255, 255, 255, 0);
  transform: translateY(0%);
}

.our-services__card:hover > .our-services__card-caption p {
  opacity: 1;
}
.our-services__card-caption-text-wrapper {
  margin-top: 0;
}

</style>
