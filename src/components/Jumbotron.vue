<template>
   <section class="text-center">

      <div class="title">
         <h1 class="fw-bold">Learn At Your Own Pace!</h1>

         <p>Get teamed up with people of the same will.</p>

         <button class="btn-custom"><a href="#">Get started for free</a></button>
      </div>
      
      <div class="jumbo-images d-flex justify-content-between align-items-center">
         <img class="left-person" src="../assets/img/home-6-hero-left-person.png" alt="left person">
         <img src="../assets/img/home-6-hero-right-person.png" alt="right person" class="right-person">
         <div class="preview-youtube-image">
            <img src="../assets/img/home-6-hero-poster-final.jpg" alt="home poster">
            <img class="play-youtube" src="../assets/img/icon-youtube-play.png" alt="youtube play">
         </div>
      </div>

   </section>
</template>

<script>
export default {
   name: 'Jumbotron'
}
</script>

<style lang="scss" scoped>

@import '../assets/style/mixins.scss';

   section {

      .title {
         margin-top: 70px;
      
         h1 {
            @include title();
         }
         p {
            @include subTitle('white');
            font-size: 1rem;
         }
         button {
            margin: 10px 0;
         }
      }

      .jumbo-images {
         width: 1400px;
         max-width: 100%;
         height: 380px;
         margin: 0 auto;
         position: relative;
         overflow: hidden;
         transform: translateY(65px);

         .preview-youtube-image {
            height: 350px;

            display: inline-block;
            position: absolute;
            @include positionCenter;
            box-shadow: 0px 5px 17px -5px rgba(0,0,0,0.46);

            border: 15px solid #fff;
            border-radius: 10px;
            cursor: pointer;
            
            img {
               height: 100%;
               object-fit: cover;
               object-position: center;
            }
            .play-youtube {
               height: 50px;
               position: absolute;
               @include positionCenter;
            }
         }
         
         .left-person {
            height: 380px;
            transform: translateX(142px);
         }

         .right-person {
            height: 220px;
            align-self: flex-end;
            transform: translate(-263px, 47%);
         }
      }
   }
</style>