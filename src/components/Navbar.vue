<template>
   <nav class="container d-flex justify-content-between align-items-center">

      <div class="logo">
         <a href="#">
            <img src="../assets/img/light-logo.png" alt="logo max coach">
         </a>
      </div>

      <div class="nav-bar-custom d-flex align-items-center">
         <!-- nav list -->
         <ul class="m-0">
            <li
               v-for="(navItem, index) in navList"
               :key="index"
               class="nav-item d-inline-block"
            >
               <a class="text-white" href="#">{{ navItem }}</a>
               <i class="fas fa-chevron-down"></i>
            </li>
         </ul>

         <!-- carrello e profilo -->
         <div class="user d-flex">

            <div class="shopping-cart me-4">
               <i class="fas fa-shopping-cart"></i>
               <div class="shopping-count">0</div>
            </div>

            <div class="profile me-4">
               <i class="far fa-user"></i>
            </div>

         </div>

         <!-- search bar -->
         <div class="search-bar d-flex">
            <input type="text" class="form-control" placeholder="Search...">
            <div class="lens-icon">
               <i class="fas fa-search"></i>
            </div>
         </div>
      </div>

   </nav>
</template>

<script>
export default {
   name: 'Navbar',
   props: {
      navList: Array
   }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';

   nav {
      padding: 15px;

      .logo {
         width: 200px;

         img {
            width: 100%;
         }
      }

      .nav-item {
         margin-right: 30px;
         text-transform: capitalize;

         &:last-child {
            margin: 0;
         }

         .fas {
            padding: 0 3px;
            font-size: 10px;
            cursor: pointer;
            vertical-align: middle;
         }
      }

      .user {
         cursor: pointer;

         .shopping-cart {
            position: relative;

            i {
               font-size: 20px;
               vertical-align: middle;
            }
            
            .shopping-count {
               width: 18px;
               height: 18px;
      
               position: absolute;
               top: -12px;
               right: -12px;

               font-size: 13px;
               text-align: center;
               color: $port-gore;
               border-radius: 50%;
               background-color: #fff;
            }
         }

         .profile {
            width: 26px;
            height: 26px;
            text-align: center;
            border: 3px solid #fff;
            border-radius: 50%;
         }
      }

      .search-bar {
         width: 210px;
         height: 50px;

         input {
            width: 80%;
            padding: 10px 15px;

            border: 0;
            border-radius: 0;
            border-top-left-radius: 6px;
            border-bottom-left-radius: 6px;

            &:focus {
               outline: 0;
               box-shadow: none;
               border: 0;
            }
         }

         .lens-icon {
            width: 20%;
            display: grid;
            place-items: center;

            color: $jungle-green;
            background-color: #fff;
            border-top-right-radius: 6px;
            border-bottom-right-radius: 6px;
            cursor: pointer;
         }
      }
   }
</style>