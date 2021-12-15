<template>
   <section>

      <div class="title text-center">
         <h4 class="fw-bold">Start today for getting <span class="evidence">Online Certification</span></h4>
         <h3 class="fw-bold">You can be your own guiding star with our help!</h3>
      </div>

      <div class="d-flex justify-content-center my-5">
         <button class="btn-custom"><a href="#">Get started now</a></button>
      </div>

   </section>
</template>

<script>
export default {
   name: 'GetStarted'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

   section {
      padding: 100px 0;

      .title {

         h4,
         .evidence {
            @include title('sm')
         }
         h3 {
            @include title('md')
         }
      }
   }

</style>