<template>
   <section class="courses">

      <div class="title text-center">
         <span class="text-uppercase upper-subtitle">choose a course to get started</span>
         <h2 class="text-capitalize title-section">latest feature <span class="evidence">courses</span></h2>
      </div>

      <div class="container">
         <div class="row myCards">
            <div 
               class="col-6"
               v-for="(course, index) in courses"
               :key="index"
            >
               <div class="myCard d-flex">
                  <div class="image">
                     <img :src="course.imgPath" alt="person">
                  </div>
                  <div class="captions">
                     <span class="price" v-if="course.price.toLowerCase() !== 'free'">
                        ${{ course.price }}<!--
                        --><span class="decimals">.00</span>
                     </span>
                     <span class="price text-capitalize" v-else>{{ course.price }}</span>
                     <p>{{ course.caption }}</p>
                     <span class="info-span">
                        <i class="far fa-file-alt"></i>
                        {{ course.lessons }} Lessons
                     </span>
                     <span class="info-span">
                        <i class="far fa-user"></i>
                        {{ course.students }} Students
                     </span>
                  </div>
               </div>
            </div>
         </div>
         <div class="d-flex justify-content-center">
            <button class="btn-custom"><a href="#">View all courses <i class="fas fa-long-arrow-alt-right"></i></a></button>
         </div>
      </div>

   </section>
</template>

<script>
export default {
   name: 'Courses',
   props: {
      courses: Array
   }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   section.courses {
      padding: 90px 0;
      background-color: $bg-color-gray;
      
      .myCards {
         margin: 60px 0;

         .myCard {
            margin: 35px 0;
            padding: 10px;
            cursor: pointer;
            transition: $transition;

            &:hover {
               background-color: #fff;
               box-shadow: $shadow;
               border-radius: 6px;
            }
            .image {
               width: 170px;
               height: 170px;
               margin: 0 30px;
               border-radius: 50%;
               overflow: hidden;
               img {
                  width: 100%;
                  height: 100%;
                  object-fit: cover;
               }
            }
         
            .captions {
               width: calc(100% - 230px);
               .price {
                  @include title('sm');
                  font-weight: bold;
                  color: $jungle-green;
                  .decimals {
                     font-size: 1rem;
                  }
               }
               p {
                  color: $port-gore;
                  font-weight: bold;
                  font-size: 1.3rem;
               }
               
            }
         }
      }

      button i {
         vertical-align: middle;
         font-size: 1.1rem;
      }
   }

</style>