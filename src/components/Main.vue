<template>
   <main>

      <Service :objectsLearned="objectsLearned" :serviceCaptions="serviceCaptions" />

   </main>
</template>

<script>
import Service from './Service.vue'
export default {
   name: 'Main',
   components: {
      Service
   },
   data() {
      return {
         objectsLearned: [
            {
               type: 'finished sessions',
               count: '1.926'
            },
            {
               type: 'enrolled learners',
               count: '3.092+'
            },
            {
               type: 'online instructors',
               count: '200'
            },
            {
               type: 'satisfaction rate',
               count: '100%'
            },
         ],
         serviceCaptions: [
            {
               title: 'graphic design',
               caption: 'Have a passion for graphics and arts? Show your talents with confidence and self-assertiveness.',
               imgPath: require('../assets/img/home-6-service-image-01.png'),
            },
            {
               title: 'business administration',
               caption: 'Learners are encouraged to study the mechanism and structure of system administration.',
               imgPath: require('../assets/img/home-6-service-image-02.png'),
            },
            {
               title: 'Idea Discussion',
               caption: 'Get teamed up with the specialists who work and teach coding for year at foamous univerities',
               imgPath: require('../assets/img/home-6-service-image-03.png'),
            },
            {
               title: 'web development',
               caption: 'Learn to start building a webpage from scratch. You decide your own pace, course, and speed.',
               imgPath: require('../assets/img/home-6-service-image-04.png'),
            },
         ],
      }
   }
}
</script>

<style lang="scss">

@import '../assets/style/mixins.scss';


</style>