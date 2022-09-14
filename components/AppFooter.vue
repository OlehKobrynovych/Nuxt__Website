<template>
    <div class="app-footer" >
        <div class="app-footer--wrap container" >
            <div class="app-footer__logo">Назва Сайту</div>
            <div class="app-footer__main">© 2022 | назва сайту</div>
            <router-link class="app-footer__btn" to="/policy">Політика конфіденційності</router-link>
        </div>
    </div>
</template>

<script>

export default {
  name: 'IndexPage',

  data() {
      return {
          // isOpen: false,
      }
  },
  methods: {
      // onOpen() {
      //     this.isOpen = !this.isOpen; 
      // }
  },
}
</script>

<style>

.app-footer {
    padding-top: 18px;
    padding-bottom: 18px;
}

.app-footer--wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.app-footer__logo {
}

.app-footer__main {

}

.app-footer__btn {
    border: none;
    color: white;
    padding: 14px 28px;
    font-size: 16px;
    cursor: pointer;
    border-radius: 7px;
    background-color: #e7e7e7; color: black;
    transition: .3s;
}

.app-footer__btn:hover {
    background: #ddd;
    scale: 1.1;
}

</style>
