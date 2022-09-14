<template>
    <div class="portfolio-slider" id="portfolio">
      
        <div class="portfolio-slider__container container">
            <h4 class="portfolio-slider__container-title">ПОРТФОЛІО</h4>
            <div class="portfolio-slider__item fade">
                <div class="portfolio-slider__item-wrap">
                    <img class="portfolio-slider__item-image" src="https://cdn.pixabay.com/photo/2017/02/01/22/02/mountain-landscape-2031539_960_720.jpg">
                    <div class="portfolio-slider__item-content">
                        <div class="portfolio-slider__item-title">Лендінг</div>
                        <div class="portfolio-slider__item-text">Розробка сайту для шкколи іноземних мов. Складається з двох посадкових сторінок</div>
                        <a href="#" class="portfolio-slider__item-readmore">Read More</a>
                    </div>
                </div>
            </div>

            <div class="portfolio-slider__item fade">
                <div class="portfolio-slider__item-wrap">
                    <img class="portfolio-slider__item-image" src="https://cdn.pixabay.com/photo/2017/02/01/22/02/mountain-landscape-2031539_960_720.jpg">
                    <div class="portfolio-slider__item-content">
                        <div class="portfolio-slider__item-title">Корпоративний сайт</div>
                        <div class="portfolio-slider__item-text">Корпоративний сайт виробника паркетної дошки з каталогу продукції</div>
                        <a href="#" class="portfolio-slider__item-readmore">Read More</a>
                    </div>
                </div>
            </div>

            <div class="portfolio-slider__item fade">
                <div class="portfolio-slider__item-wrap">
                    <img class="portfolio-slider__item-image" src="https://cdn.pixabay.com/photo/2017/02/01/22/02/mountain-landscape-2031539_960_720.jpg">
                    <div class="portfolio-slider__item-content">
                        <div class="portfolio-slider__item-title">Лендінг</div>
                        <div class="portfolio-slider__item-text">Мультимовний лендинг із можливістю донату. Підключено платіжну систему</div>
                        <a href="#" class="portfolio-slider__item-readmore">Read More</a>
                    </div>
                </div>
            </div>

            <a class="portfolio-slider__prev-btn" @click="plusSlides(-1)">❮</a>
            <a class="portfolio-slider__next-btn" @click="plusSlides(1)">❯</a>

        </div>
        <br>
    </div>
</template>



<script>

export default {

  data() {
      return {
          slideIndex: 1,
      }
  },

  mounted() {
        this.showSlides(this.slideIndex);
  },
  
  methods: {
    showSlides(n) {
        let i;
        let slides = document.getElementsByClassName("portfolio-slider__item");
        if (n > slides.length) {this.slideIndex = 1}    
        if (n < 1) {this.slideIndex = slides.length}
        for (i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";  
        }
        slides[this.slideIndex-1].style.display = "block";  
    },

    plusSlides(n) {
        this.showSlides(this.slideIndex += n);
    },
  },
}
</script>

<style>
.portfolio-slider {
    padding: 20px 0;
}

.portfolio-slider__item {display: none;}

.portfolio-slider__container {
  max-width: 1000px;
  position: relative;
  margin: auto;
}

.portfolio-slider__container-title {
    text-align: center;
    font-size: 22px;
    display: block;
    margin-top: 25px;
    margin-bottom: 20px;
}

.portfolio-slider__prev-btn, .portfolio-slider__next-btn {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 16px;
  margin-top: -22px;
  color: white;
  background: #909198;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}

.portfolio-slider__next-btn {
  right: 0;
  border-radius: 3px 0 0 3px;
}

.portfolio-slider__prev-btn {
  left: 0;
  border-radius: 3px 0 0 3px;
}

.portfolio-slider__prev-btn:hover, .portfolio-slider__next-btn:hover {
  background-color: rgba(0,0,0,0.8);
}

.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {opacity: .4;}
  to {opacity: 1;}
}

@media only screen and (max-width: 300px) {
  .portfolio-slider__prev-btn, .portfolio-slider__next--btn {font-size: 11px;}
}


/* ------------------- */

.portfolio-slider__item-wrap {
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(200px, 1fr));
    background:#0002;
    border-radius: 0.75em;
    border:1px solid #ffffff90;
    box-shadow: 
        0 2px 1px 1px rgba(0, 0, 0,.09), 
    0 5px 4px 1px rgba(0, 0, 0, 0.15), 
    0 7px 10px -3px rgba(0, 0, 0,0.17), 
    0 10px 13px -4px rgba(0, 0, 0, 0.23), 
    0 16px 20px -4px rgba(0, 0, 0, 0.36);
    overflow:hidden;
} 

.portfolio-slider__item-image {
    padding: 0.5em;  
    display:flex;
    object-fit:cover;
    height:100%;
    max-width:100%;
}

.portfolio-slider__item-content {
    display: flex;
    flex-direction: column;
    margin: 1em; 
    justify-content:center;
}

.portfolio-slider__item-title {
    font-weight:700;
    font-family:sans-serif;
    font-size: clamp(1.3rem, 2.5vw, 1.6rem);
    text-align:center;
    margin-bottom:1em;
}

.portfolio-slider__item-text {
    max-width:50ch;
    color:#0006;
    margin-bottom: 1em;
} 

.portfolio-slider__item-readmore {
    text-decoration:none;
    color:white;
    display:inline-flex;
    padding: 0.25em 1.15em;
    border-radius: 0.6em;
    width:max-content;
    background: teal;
    margin-left: auto;
    box-shadow:
    0 1px 2px 0 #0003, 
    0 3px 7px 0 #0004, 
    0 8px 15px 0 #0005;
 } 

.portfolio-slider__item-readmore:hover {
    scale: 1.05;
} 

</style>
