<template>
    <div class="contact-form" id="contact">
        <h3 class="contact-form__title">Контакти</h3>

        <div class="contact-form--wrap container">
            <div class="contact-form__info">
                <div class="contact-form__info-geo">
                    <span>Місцезнаходженн: </span>
                    Україна, Львів вул. Євгена Сверстюка, 19
                </div>
                <div class="contact-form__info-tel">
                    <span>Телефон: </span>
                    121354578785
                </div>
                <div class="contact-form__info-mail">
                   <span>Емейл: </span> 
                   asds@gmail.com
                </div>
                <div class="contact-form__info-social">
                    <a class="contact-form__info-social-link" href="#" target="_blank"><img src="icons/Telegram.svg" alt="img" /></a>
                    <a class="contact-form__info-social-link" href="#" target="_blank"><img src="icons/Viber.svg" alt="img" /></a>
                </div>
            </div>

            <form class="contact-form__form" action="">
                <label for="fname">Ваше ім'я</label>
                <input type="text" id="fname" name="firstname" placeholder="Введіть Ваше ім'я...">

                <label for="lname">Ваш емейл</label>
                <input type="mail" id="mail" name="mail" placeholder="Введіть Ваш емейл...">

                <label for="subject">Ваше повідомлення</label>
                <textarea id="subject" name="subject" placeholder="ВВедіть Ваше повідомлення..." style="height:200px"></textarea>

                <input class="contact-form__submit-btn" type="submit" value="Submit">
            </form>
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

<style>
.contact-form {

}

.contact-form__title {
    text-align: center;
    font-size: 20px;
    margin-top: 30px;
    margin-bottom: 20px;
}

.contact-form--wrap {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 15px;
    border-radius: 5px;
    background-color: #f2f2f2;
    padding: 20px;
}

.contact-form__info {
    margin-bottom: 30px;
    width: 100%;
}

.contact-form__info-geo {
    margin-bottom: 15px;
}

.contact-form__info-tel {
    margin-bottom: 15px;

}

.contact-form__info-mail {
    margin-bottom: 15px;
}

.contact-form__info-social {
    display: flex;
    gap: 20px;
}

.contact-form__info-social-link {
    transition: .3s;
}

.contact-form__info-social-link:hover {
    scale: 1.08;
}

.contact-form__form {
    width: 100%;
}

input[type=text], input[type=mail], textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}

.contact-form__submit-btn {
  background-color: #ddd;
  border: none;
  border-radius: 7px;
  color: black;
  padding: 16px 32px;
  text-align: center;
  font-size: 16px;
  margin: 4px 2px;
  transition: 0.3s;
}

.contact-form__submit-btn:hover {
    background-color: #9d9a9a;
    color: white;
}

@media (min-width: 576px) {
    .contact-form--wrap {
        flex-direction: row;
    }

    .contact-form__info {
        width: 50%;
    }

    .contact-form__form {
        width: 50%;
    }
 
}
  
@media (min-width: 768px) {
   
}

</style>
