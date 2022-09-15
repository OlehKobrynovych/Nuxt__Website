<template>
    <div class="app-header">
        <div class="app-header-wrap container">
            <router-link class="app-header__logo" to='/'>Назва фірми</router-link>
            <div class="app-header__menu">
                <ul class="app-header__menu-wrap">
                    <li><router-link class="app-header__menu-item" to="/">Про нас</router-link></li>
                    <li><router-link class="app-header__menu-item" to="#services">Послуги</router-link></li>
                    <li><router-link class="app-header__menu-item" to="#contact">Контакти</router-link></li>
                    <li><router-link class="app-header__menu-item" to="#portfolio">Портфоліо</router-link></li>
                </ul>
            </div>
            <MobileMenu @click.native="onOpen" />
        </div>

        <div 
            class="app-header__sidebar-menu"
            :class="{'app-header__sidebar-menu--activ': isOpen}"
        >
            <ul>
                <li><router-link class="app-header__sidebar-menu-linc" to="/" @click.native="onOpen">Про нас</router-link></li>
                <li><router-link class="app-header__sidebar-menu-linc" to="#services" @click.native="onOpen">Послуги</router-link></li>
                <li><router-link class="app-header__sidebar-menu-linc" to="#contact" @click.native="onOpen">Контакти</router-link></li>
                <li><router-link class="app-header__sidebar-menu-linc" to="#portfolio" @click.native="onOpen">Портфоліо</router-link></li>
            </ul>
        </div>

    </div>
</template>

<script>
import MobileMenu from './MobileMenu.vue'
export default {
  components: { MobileMenu },

   data() {
      return {
          isOpen: false,
      }
  },
  methods: {
      onOpen() {
          this.isOpen = !this.isOpen; 
      }
  },
}
</script>

<style scoped>
.app-header {
    position: sticky;
    top: 0;
    left: 0;
    background: #babebc;
    z-index: 11;
    /* padding: 1rem 0; */
    /* border-bottom: 1px solid #000; */
    /* box-shadow: 0 0 5px 2px #000; */
}

.app-header-wrap {
    position: relative;
    background: #fff;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-top: 1rem;
    padding-bottom: 1rem;
    /* border-bottom: 1px solid #000; */
    /* box-shadow: 0 0 5px 2px #000; */
    box-shadow: -5px -5px 10px #fff, 5px 5px 10px #babebc;
    z-index: 10;
}

.app-header__logo {
    transition: .3s;
}

.app-header__logo:hover {
    scale: 1.15;
}

.app-header__menu {
    display: none;
}

.app-header__menu-wrap {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.app-header__menu-item {
    margin-left: 15px;
    transition: .3s;
}

.app-header__menu-item:hover {
    scale: 1.15;
    color: rgb(11, 11, 244);
}

/* ----------- */


.app-header__sidebar-menu {
    position: fixed;
    top: 0;
    right: -150%;
    width: 100%;
    height: 100vh;
    background: #fff;
    box-shadow: -5px -5px 10px #fff, 5px 5px 10px #babebc;
    padding-top: 120px;
    z-index: 4;
    transition: 1.5s;
    text-align: center;
}

.app-header__sidebar-menu--activ {
    right: 0;
}

.app-header__sidebar-menu-linc {
    display: inline-block;
    text-align: center;
    color: #000;
    font-size: 25px;
    font-weight: bold;
    cursor: pointer;
    margin-bottom: 20px;
    transition: .5s;
}

.app-header__sidebar-menu-linc:hover {
    scale: 1.15;
    color: rgb(11, 11, 244);
}



@media (min-width: 576px) {
  .app-header__menu {
    display: block;
}
}
  
@media (min-width: 768px) {
  
}


</style>

