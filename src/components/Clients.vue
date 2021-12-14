<template>
   <section class="clients-testimonial">

      <div class="title">
         <h2 class="title-section text-center">Why People Talk About <span class="evidence">MaxCoach</span>?</h2>
      </div>
      
      <div class="talk-about container">
         <div class="row testimonial">
            <div class="col-4 d-flex justify-content-center">
               <div class="ball"></div>
               <div class="ball"></div>
               <div class="ball"></div>
               <div class="myImage">
                  <img src="../assets/img/testimonial-avata-02.jpg" alt="testimonial">
               </div>
            </div>
            <div class="col-8">
               <h3>I am free to learn at my own pace, follow my own schedule and choose the subject I like. Great study protal for people like me.</h3>
               <p class="text-uppercase fw-bold">mina hollace</p>
               <span>/Freelancer</span>
            </div>
         </div>
         <div class="row clients">
            <div 
               class="col-2  d-flex justify-content-center align-items-center"
               v-for="(client, index) in clients"
               :key="index"
            >
               <div class="myImage">
                  <img :src="client" alt="client">
               </div>
            </div>
         </div>
      </div>

   </section>
</template>

<script>
export default {
   name: 'Clients',
   props: {
      clients: Array
   }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   section.clients-testimonial {
      padding: 50px 0;

      .talk-about {
         
         .testimonial {
            padding: 80px;
            
            .col-4 {
               background-image: url(../assets/img/maxcoach-shape-05-100x100.png);
               background-repeat: no-repeat;
               background-position: bottom;
               background-position-x: 215px;
               position: relative;

               .ball {
                  width: 75px;
                  height: 75px;

                  position: absolute;

                  border-radius: 50%;
                  background-color: #D2A98E;
                  &:first-child {
                     top: -10px;
                     left: 130px;
                  }
                  &:nth-child(2) {
                     top: 40px;
                     left: 95px;
                  }
                  &:nth-child(3) {
                     top: 10px;
                     right: 115px;
                  }
               }
               .myImage {
                  width: 200px;
                  height: 200px;
                  border-radius: 50%;
                  overflow: hidden;
                  z-index: 100;
                  img {
                     height: 100%;
                  }
               }
            }
         
            h3 {
               @include title('md');
               margin-bottom: 50px;
            }
            span {
               @include subTitle();
            }
         }

         .clients {
            margin-bottom: 30px;
            
         }
      }
   }
</style>