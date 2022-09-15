<template>
    <div class="more-question">
        <div class="more-question--wrap container">
            <h3 class="more-question__title">Часті питання про створення сайтів</h3>
            <div v-for="question of question" :key="question.id">
                <button class="more-question__accordion" :class="{'more-question__active': question.isOpen}" @click="onOpen(question)">{{question.title}}</button>
                <div 
                    class="more-question__panel"
                    :class="{'more-question__panel--active': question.isOpen}"
                >
                    <p>{{question.text}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {

  data() {
      return {
          question: [
              {id: 1, title: ' Що означає замовити сайт під ключ?', text: 'Створення сайту під ключ передбачає повну розробку проекту та його реалізацію, а також просування у Мережі.', isOpen: false},
              {id: 2, title: 'Що входить у створення сайту під ключ?', text: 'У послугу створення сайту під ключ входить: підготовча аналітика, розробка дизайну, верстка, програмування, налаштування інтеграції, наповнення сайту контентом.', isOpen: false},
              {id: 3, title: 'Як відбувається розробка сайту?', text: 'У цілому нині процес розробки сайту складається з наступних етапів: аналіз ЦА, створення прототипу, розробка дизайну, безпосередня розробка сайту.', isOpen: false},
              {id: 4, title: 'Скільки часу займає розробка сайту?', text: 'Термін розробки невеликого сайту складає 2-4 тижні. Якщо йдеться про великий інтернет-портал, то на це потрібно 3 місяці. В цілому робота по кожному проекту індивідуальна і витрати часу на розробку сайту розраховуються окремо в кожному випадку.', isOpen: false},
          ],
      }
  },
  methods: {
      onOpen(question) {
          question.isOpen = !question.isOpen;
        //   this.question = this.question.map(el => {
        //       if(el.id == id) {
        //           el.isOpen = !el.isOpen;
        //       } else {
        //         //   el.isOpen = false;
        //       }
        //       return el
        //   }); 
      }
  },
}
</script>

<style>

.more-question {

}

.more-question--wrap {

}

.more-question__title {
    display: block;
    margin: 15px 0;
}

.more-question__accordion {
  background-color: #eee;
  color: #444;
  cursor: pointer;
  padding: 18px;
  width: 100%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 15px;
  transition: 0.4s;
}

.more-question__active, .more-question__accordion:hover {
  background-color: #ccc;
}

.more-question__accordion:after {
  content: '\002B';
  color: #777;
  font-weight: bold;
  float: right;
  margin-left: 5px;
}

.more-question__active:after {
  content: "\2212";
}

.more-question__panel {
  padding: 0 18px;
  background-color: white;
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s ease-out;
}

.more-question__panel p {
  padding: 10px 0;
}

.more-question__panel--active {
  max-height: 500px;
}

@media (min-width: 576px) {
 
}
  
@media (min-width: 768px) {
   
}

</style>
