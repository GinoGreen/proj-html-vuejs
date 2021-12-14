<template>
   <section class="service">

      <div class="title container">
         <h3 class="fw-bold">Let passion and determination be the guide along the way and develop at your own pace that's comfortable.</h3>
         <p class="text-uppercase">fannie moreno</p>
         <span>/Founder & CEO</span>
      </div>

      <div class="object-learned container">
         <div class="row">
            <div 
               class="item col-3 text-center"
               v-for="(object, index) in objectsLearned"
               :key="`objectsLearned ${index}`"
            >
               <p class="object-count">{{ object.count }}</p>
               <p class="object-type text-uppercase">{{ object.type }}</p>
            </div>
         </div>
      </div>

      <div class="get-start container">
         <div class="row">
            <!-- img card -->
            <div class="col-6">
               <!-- nesting -->
               <div class="row">
                  <div 
                     class="col-6 dad"
                     v-for="(service, index) in serviceCaptions"
                     :key="`serviceCaptions ${index}`"
                  >
                     <div class="myCard">
                        <div class="text">
                           <h4 class="text-capitalize">{{ service.title }}</h4>
                           <p>{{ service.caption }}</p>
                        </div>
                        <img :src="service.imgPath" alt="persons">
                     </div>
                  </div>
               </div>
            </div>
            <!-- can provide get started for free -->
            <div class="col-6"></div>
         </div>
      </div>

   </section>
</template>

<script>
export default {
   name: 'Service',
   props: {
      objectsLearned: Array,
      serviceCaptions: Array
   }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   section.service {

      .title {
         max-width: 700px;
         margin: 200px auto 100px;
         text-align: center;
         
         h3 {
            margin: 40px;
            line-height: 46px;
         }
         p {
            margin: 2px 0;
            font-size: 0.8rem;
            font-weight: bold;
         }
         span {
            @include subTitle();
         }
      }

      .object-learned {
         
         .object-count {
            font-size: 2.2rem;
            font-weight: bold;
            color: $jungle-green;
         }
         .object-type {
            @include subTitle;
            font-weight: bold;
            font-size: .8rem;
            letter-spacing: 0.1em;
         }
      }

      .get-start {
         margin: 240px auto;
         
         .dad {
            
            .myCard {
               height: 422px;
               margin: 14px 0;
               padding: 35px 20px 20px;
               position: relative;

               border-radius: 6px;
               box-shadow: 0px 0px 27px 2px rgba(0,0,0,0.14);
               overflow: hidden;
   
               h4 {
                  @include title('sm');
                  font-weight: bold;
               }
   
               img {
                  width: 100%;
                  position: absolute;
               }
            }
            &:first-child .myCard img {
               width: 285px;
               bottom: 0;
               left: 0;
            }
            &:nth-child(2) .myCard img {
               width: 195px;
               bottom: 0;
               left: 50%;
               transform: translateX(-50%);
            }
            &:nth-child(3) .myCard,
            &:last-child .myCard {
               .text {
                  transform: translateY(180%);
               }
            }
            &:nth-child(3) .myCard img {
               width: 57%;
               left: 0;
               top: 16px;
            }
            &:last-child .myCard img {
               width: 85%;
               top: 22px;
            }

            // translate dispari
            &:nth-child(odd) {
               transform: translateY(-15%);
            }
         }
      }
   }
</style>