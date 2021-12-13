<template>
   <nav class="container d-flex justify-content-between">
      <div class="logo">
         <a href="#">
            <img src="../assets/img/light-logo.png" alt="logo max coach">
         </a>
      </div>
   </nav>
</template>

<script>
export default {
   name: 'Navbar'
}
</script>

<style lang="scss">

   nav {
      padding: 15px;

      .logo {
         width: 200px;

         img {
            width: 100%;
         }
      }
   }
</style>