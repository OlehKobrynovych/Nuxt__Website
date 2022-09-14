<template>
    <div class="work-phase">
        <h4 class="work-phase__title">ЕТАПИ РОБОТИ</h4>
        <div class="work-phase__timeline">
            <div class="work-phase__item work-phase__item-left">
                <div class="work-phase__item-wrap">
                <h2 class="work-phase__item-title">ОБГОВОРЕННЯ</h2>
                <p>Ми домовимося з вами про дзвінок, щоб познайомитися та детальніше обговорити проект та завдання, які нам потрібно буде вирішити. В результаті ми визначимо обсяг робіт і на підставі цього я зможу розрахувати вартість та строки.</p>
                </div>
            </div>
            <div class="work-phase__item work-phase__item-right">
                <div class="work-phase__item-wrap">
                <h2 class="work-phase__item-title">СТВОРЕННЯ ПРОТОТИПУ</h2>
                <p>Прототип – це схематичне зображення кожної сторінки сайту, без дизайну та фотографій. Для прототипу вам потрібно буде надати текстовий контент. Я не пишу тексти з нуля, але можу допомогти вам відредагувати ваші.</p>
                </div>
            </div>
            <div class="work-phase__item work-phase__item-left">
                <div class="work-phase__item-wrap">
                <h2 class="work-phase__item-title">ДИЗАЙН УСЬОГО САЙТУ</h2>
                <p>На основі затвердженої дизайн-концепції я розробляю дизайн усіх сторінок/блоків сайту та презентую його вам.</p>
                </div>
            </div>
            <div class="work-phase__item work-phase__item-right">
                <div class="work-phase__item-wrap">
                <h2 class="work-phase__item-title">АДАПТИВНА ВЕРСТКА</h2>
                <p>Повністю затверджений дизайн я переношу в CMS та адаптую його під 5 дозволів екранів. Підключаю форми для прийому заявок та всі необхідні сервіси. Налаштовую базове SEO.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
 
}
</script>

<style>

.work-phase {
    position: relative;
    max-width: 1200px;
    margin: 0 auto;
    background: #000;
    overflow: hidden;
}

.work-phase__title {
    text-align: center;
    color: #fff;
    font-size: 20px;
    margin-top: 30px;
    margin-bottom: 10px;
}

.work-phase__timeline::after {
    left: 31px;
}

.work-phase::after {
    display: block;
    content: '';
    position: absolute;
    width: 6px;
    background-color: white;
    top: 81px;
    bottom: 0;
    left: 50%;
    margin-left: -3px;
}

.work-phase__item {
    padding: 10px 40px;
    position: relative;
    background-color: inherit;
    width: 50%;
}

.work-phase__item::after {
    content: '';
    position: absolute;
    width: 25px;
    height: 25px;
    right: -12px;
    background-color: white;
    border: 4px solid #FF9F55;
    top: 15px;
    border-radius: 50%;
    z-index: 1;
}

.work-phase__item-left {
left: 0;
}

.work-phase__item-right {
    left: 50%;
}

.work-phase__item-left::before {
    content: " ";
    height: 0;
    position: absolute;
    top: 22px;
    width: 0;
    z-index: 1;
    right: 30px;
    border: medium solid white;
    border-width: 10px 0 10px 10px;
    border-color: transparent transparent transparent white;
}

.work-phase__item-right::before {
    content: " ";
    height: 0;
    position: absolute;
    top: 22px;
    width: 0;
    z-index: 1;
    left: 30px;
    border: medium solid white;
    border-width: 10px 10px 10px 0;
    border-color: transparent white transparent transparent;
}

.work-phase__item-right::after {
    left: -12px;
}

.work-phase__item-wrap {
    padding: 20px 30px;
    background-color: white;
    position: relative;
    border-radius: 6px;
}

.work-phase__item-title {
    margin-bottom: 8px;
}

@media (max-width: 600px) {
  /* .work-phase__timeline::after {
  left: 31px;
  } */

    .work-phase::after {
        display: none;
    }
  
    .work-phase__item {
        width: 100%;
        padding-left: 70px;
        padding-right: 25px;
    }
  
    .work-phase__item::before {
        left: 60px;
        border: medium solid white;
        border-width: 10px 10px 10px 0;
        border-color: transparent white transparent transparent;
    }

    .work-phase__item-left::after, .work-phase__item-right::after {
        left: 15px;
    }
  
    .work-phase__item-right {
        left: 0%;
    }
}
</style>
