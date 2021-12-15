<template>
   <footer>
      <div class="container">

         <div class="row">

            <div class="col-6">
               <h5 class="fw-bold">Address</h5>
               <p class="my-3">382 NE 191st St # 87394 Miami, FL 33179-3899</p>
               <p class="my-3">+1 (305) 547-9909 (9am - 5pm EST, Monday -Friday)</p>
               <p class="my-3">support@maxcoach.com</p>
               <!-- icons socials -->
               <div class="socials">
                  <i class="fab fa-facebook-square"></i>
                  <i class="fab fa-twitter"></i>
                  <i class="fab fa-instagram"></i>
                  <i class="fab fa-linkedin"></i>
               </div>
            </div>

            <div class="col-6">
               <!-- nesting -->
               <div class="row lists">
                  <div 
                     class="col-3"
                     v-for="(list, index) in footerLists"
                     :key="`footerLists ${index}`"
                  >
                     <h5 class="fw-bold text-capitalize">{{ list.title }}</h5>
                     <ul>
                        <li
                           class="my-3"
                           v-for="(item, index) in list.voices"
                           :key="`voices ${index}`"
                        >
                           {{ item }}
                        </li>
                     </ul>
                  </div>
               </div>
            </div>

         </div>

         <p class="text-center mt-5 copyright">&copy; 2020 Maxcoach. All Right Reserved</p>

      </div>
   </footer>
</template>

<script>
export default {
   name: 'Footer',
   props: {
      footerLists: Array
   }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   footer {
      padding: 70px 0 30px;
      background-color: $bg-color-gray;

      .socials {
         color: $soft-grey;
         font-size: 32px;
         i {
            margin: 20px 40px 20px 0;
         }
      }

      h5 {
         min-height: 30px;
      }
      li {
         cursor: pointer;
         &:hover {
            text-decoration: underline;
         }
      }

      .copyright {
         color: $soft-grey;
      }
   }
</style>