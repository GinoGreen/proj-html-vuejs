<template>
   <section>

      <div class="title text-center">
         <span class="text-uppercase upper-subtitle">wanna tranform your life?</span>
         <h2 class="title-section">Glad to <span class="evidence">Help You</span> Learn</h2>
      </div>

      <div class="container">
         <div class="row helps">
            <div 
               class="col-3"
               v-for="(help, index) in helps"
               :key="index"
            >
               <div class="help">
                  <div class="myImage"> 
                     <img :src="help.imgPath" alt="icon">
                  </div>
                  <h4 class="fw-bold text-capitalize">{{ help.title }}</h4>
                  <p>{{ help.caption }}</p>
               </div>
            </div>
         </div>
         <!-- immagine grande -->
         <div class="bigImage">
            <img src="../assets/img/home-6-services-image.png" alt="persons">
         </div>
      </div>

   </section>
</template>

<script>
export default {
   name: 'Helps',
   props: {
      helps: Array
   }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   section {
      padding: 100px 0;
      background: linear-gradient(#fff, $bg-color-gray);

      .helps {
         margin: 30px 0;
         .help {
            padding: 20px;

            .myImage {
               width: 80px;
               margin: 30px 0;
               img {
                  width: 100%;
               }
            }
            h4 {
               margin-bottom: 20px;
            }
         }
      }
      .bigImage {
         display: flex;
         justify-content: center;
         transform: translateY(calc(100px + 32px));
         img {
            width: 90%;
         }
      }
   }

</style>