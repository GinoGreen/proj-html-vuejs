<template>
   <section>

      <!-- titolo -->
      <div class="title text-center">
         <span class="text-uppercase upper-subtitle">enjoy reading on maxcoach</span>
         <h2 class="title-section">Latest on <span class="evidence">Our Blogs</span></h2>
      </div>

      <!-- articoli blog -->
      <div class="container">
         <div class="row articles">
            <div 
               class="col-4"
               v-for="(article, index) in articles"
               :key="index"
            >
               <div class="article">
                  <div class="myImage">
                     <img :src="article.imgPath" alt="poster">
                  </div>
                  <span class="text-uppercase upper-subtitle">{{ article.artist }}</span>
                  <h4 class="fw-bold">{{ article.title }}</h4>
                  <span class="info-span">
                     <i class="far fa-calendar"></i>
                     {{ article.date }}
                  </span>
                  <span class="info-span">
                     <i class="far fa-eye"></i>
                     {{ article.views }} views
                  </span>
               </div>
            </div>
         </div>
      </div>

   </section>
</template>

<script>
export default {
   name: 'Articles',
   props: {
      articles: Array
   }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   section {
      padding: 100px 0 60px;
      background-color: $bg-color-gray;

      .articles {
         margin-top: 70px;

         .article {
            cursor: pointer;
            transition: $transition;
            .myImage {
               height: 325px;
               width: 100%;
               position: relative;
               border-radius: 6px;
               overflow: hidden;
               &:hover img {
                  height: 100%;
                  filter: brightness(1);
               }
               img {
                  height: 120%;
                  position: absolute;
                  @include positionCenter;
                  transition: $transition;
                  filter: brightness(.65);
               }
            }
            span.upper-subtitle {
               margin: 20px 0;
               display: inline-block;
            }
         }
      }
   }

</style>