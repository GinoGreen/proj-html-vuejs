<template>
   <header>

      <Navbar :navList="navList" />

      <Jumbotron />

   </header>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
import Navbar from './Navbar.vue'

export default {
   name: 'Header',
   components: {
      Navbar,
      Jumbotron
   },
   data() {
      return {
         navList: ['home', 'pages', 'courses', 'features', 'blog', 'shop']
      }
   }
}
</script>

<style lang="scss">
@import '../assets/style/vars';

   header {
      color: #fff;
      background-color: $port-gore;
      position: relative;
   }
   // header::after {
   //    content: "";
   //    position: absolute;
   //    top: 100%;
   //    left: 0;
   //    height: 110px;
   //    width: 100%;
   //    background: url(../assets/img/big.svg) bottom center;
   //    background-size: cover;
   // }

</style>