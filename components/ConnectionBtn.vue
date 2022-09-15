<template>
    <div class="connection-btn" :class="{'connection-btn__open': isOpen}">
        <div class="connection-btn__item">
            <a href="#" target="_blank"><img src="icons/Viber.svg" alt="img" /></a>
        </div>
        <div class="connection-btn__item">
            <a href="#" target="_blank"><img src="icons/Telegram.svg" alt="img" /></a>
        </div>
        <div class="connection-btn__item">
            <a href="tel:+380936918890" target="_blank"><img src="icons/Telephon.svg" alt="img" /></a>
        </div>
        <button class="connection-btn__item connection-btn__item-nav" @click="onOpen">
            <svg role="presentation" class="connection-btn__svg" viewBox="0 0 35 32" xmlns="http://www.w3.org/2000/svg"> <path d="M11.2667 12.6981H23.3667M11.2667 16.4717H23.3667M4.8104 23.5777C2.4311 21.1909 1 18.1215 1 14.7736C1 7.16679 8.38723 1 17.5 1C26.6128 1 34 7.16679 34 14.7736C34 22.3804 26.6128 28.5472 17.5 28.5472C15.6278 28.5472 13.8286 28.2868 12.1511 27.8072L12 27.7925L5.03333 31V23.8219L4.8104 23.5777Z" stroke="#5ca6d1" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round" fill="none"></path> </svg>
        </button>
    </div>
</template>

<script>

export default {

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

.connection-btn {
    position: relative;
    transition: .3s;
}

.connection-btn:hover {
}

.connection-btn__item {
    display: flex;
    align-items: center;
    position: absolute;
    justify-content: center;
    width: 40px;
    height: 40px;
    padding: 7px;
    font-size: 18px;
    border-radius: 50%;
    background-color: #ebecf0;
    background-color: #ebecf0;
    text-align: center;
    cursor: pointer;
    font-weight: bold;
    transition: all 400ms ease-in-out;
}

.connection-btn__item:hover {
  scale: 1.08;
}

.connection-btn__item.connection-btn__item-nav {
  font-size: 22px;
  width: 55px;
  height: 55px;
  box-shadow: -5px -5px 10px #fff,
    5px 5px 10px #babebc;
}

.connection-btn__open .connection-btn__item {
  box-shadow: -5px -5px 10px #fff,
    5px 5px 10px #babebc;
}

.connection-btn__open .connection-btn__item.connection-btn__item-nav {
  transform: rotate(42deg);
  box-shadow: inset 7px 2px 10px #babebc,
    inset -5px -5px 12px #fff;
}

.connection-btn__open .connection-btn__item:nth-child(1) {
  transform: translate(-63px, 24px);
}

.connection-btn__open .connection-btn__item:nth-child(2) {
  transform: translate(-60px, -39px);
  transition-delay: 100ms;
}

.connection-btn__open .connection-btn__item:nth-child(3) {
  transform: translate(1px, -63px);
  transition-delay: 200ms;
}

.connection-btn__open .itconnection-btn__itemem:active {
  box-shadow: inset 1px 1px 2px #babebc,
    inset -1px -1px 2px #fff;
}
</style>
