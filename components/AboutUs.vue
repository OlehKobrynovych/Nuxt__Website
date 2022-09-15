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
    font-size: 90px;
    margin-bottom: 71px;
    background-image: url(./../static/images/3.png);
    background-position: 0px 0px;
    font-family: Impact, Charcoal, sans-serif;
            background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    -webkit-animation: animatedBackground 20s linear infinite normal;
    -webkit-box-reflect: below -39px -webkit-gradient(linear, left top, left bottom,  from(transparent), color-stop(25%, transparent), to(#FFFFFF));
    -webkit-text-stroke-width: 2px;
    -webkit-text-stroke-color: #000000;
}

@-webkit-keyframes animatedBackground {
    0% { background-position: 0 0; }
    100% { background-position: 0 -500px; }
}

.about-us__text {
    font-size: 22px;
    animation-name: fadeInLeft;
    animation-duration: 1s;
    animation-fill-mode: both;
    animation-delay: 1s;
}

@keyframes fadeInLeft {
  from {
    opacity: 0;
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
  }

  to {
    opacity: 1;
    -webkit-transform: none;
    transform: none;
  }
}


</style>
