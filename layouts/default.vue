<template>
  <div>
    <AppHeader />
    <Nuxt />
    <AppFooter />
  </div>
</template>

<script>
import AppFooter from '../components/AppFooter.vue';
import AppHeader from '../components/AppHeader.vue';
export default {
  components: { AppHeader, AppFooter },
};
</script>

<style>
html {
  margin: 0;
  padding: 0;
  height: 100%;
  min-height: 100vh;
  box-sizing: border-box;
  scroll-behavior: smooth;
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  -webkit-tap-highlight-color: transparent;
}
*,
::after,
::before {
  box-sizing: inherit;
}
*:last-child {
  margin-bottom: 0;
}
h1,
h2,
h3,
h4,
h5,
h6,
p {
  margin: 0;
  padding: 0;
  font-size: inherit;
  line-height: inherit;
  color: inherit;
}
ul,
ol,
li {
  margin: 0;
  padding: 0;
  list-style: none;
  color: inherit;
}
a {
  display: inline-block;
  text-decoration: none;
  color: inherit;
}
button,
label,
input {
  padding: 0;
  margin: 0;
  display: inline-block;
  font-size: inherit;
  line-height: inherit;
  color: inherit;
  background-color: inherit;
  border: none;
  outline: none;
  cursor: pointer;
}
img,
svg {
  margin: 0 auto;
  /* width: 100%; */
  /* height: 100%; */
  display: block;
  object-fit: cover;
  object-position: center;
}
/* textarea::-webkit-scrollbar {
  display: none;
} */
body {
  margin: 0;
  padding: 0;
  height: 100%;
  min-height: 100vh;
  font-style: normal;
  background-color: #F8F8F8;
  /* overflow-x: hidden; */
  overscroll-behavior: none;
  scroll-behavior: smooth;
}
.container {
  margin: 0 auto;
  padding: 0 18px;
  width: 100%;
  max-width: 1200px;
}
.block-wrapper {
  overflow: hidden;
}

</style>