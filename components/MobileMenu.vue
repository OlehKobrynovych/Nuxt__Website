<template>
    <div class="mobile-menu" :class="{'change': isOpen}" @click="onOpen">
        <div class="bar1"></div>
        <div class="bar2"></div>
        <div class="bar3"></div>
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

<style>
.mobile-menu {
  display: inline-block;
  cursor: pointer;
}

.bar1, .bar2, .bar3 {
  width: 26px;
  height: 4px;
  background-color: #333;
  margin: 6px 0;
  transition: 0.4s;
}

.change .bar1 {
  transform: translate(0, 11px) rotate(-45deg);
}

.change .bar2 {opacity: 0;}

.change .bar3 {
  transform: translate(0, -11px) rotate(45deg);
}

@media (min-width: 576px) {
  .mobile-menu {
      display: none;
}
}
  
@media (min-width: 768px) {
   
}

</style>
