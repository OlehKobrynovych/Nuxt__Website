<template>
    <div  class="about-us">
        <div  class="about-us--wrap  container">
            <h2 class="about-us__title">Створення сайтів</h2>
            <p class="about-us__text">Ми створюємо сайт, який дозволить розвивати ваш бізнес, використовуючи сучасні технології та досвід у сфері web-розробки.</p>
        </div>
    </div>
</template>

<script>

export default {

  data() {
      return {
        //   isOpen: false,
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
.about-us {
    width: 100vw;
    height: 100vh;
    /* background-image: url(./../static/images/1.jpg);
    background-size: cover;
    background-repeat: no-repeat; */
   background: rgb(251,248,2);
 background: linear-gradient(0deg, rgba(251,248,2,1) 0%, rgba(0,78,255,1) 100%);
}

.about-us--wrap {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    height: 100%;

    
}

.about-us__title {
    font-size: 40px;
    margin-bottom: 20px;
}

.about-us__text {
    font-size: 22px;
}

</style>
