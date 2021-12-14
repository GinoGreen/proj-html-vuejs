<template>
   <main>

      <Service :objectsLearned="objectsLearned" :servicesCaptions="servicesCaptions" :servicesList="servicesList" />

      <Courses :courses="courses" />

      <Clients :clients="clients" />

      <Articles :articles="articles" />

   </main>
</template>

<script>
import Articles from './Articles.vue'
import Clients from './Clients.vue'
import Courses from './Courses.vue'
import Service from './Service.vue'
export default {
   name: 'Main',
   components: {
      Service,
      Courses,
      Clients,
      Articles,
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
         servicesCaptions: [
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
         servicesList: [
            'Select & customize courses to your preferences',
            'Change the tuto and make arrangements',
            'Partecipate in events to join others',
            'Get the desired certificate delivered at house',
         ],
         courses: [
            {
               imgPath: require('../assets/img/course-02-480x298.jpg'),
               price: '40',
               caption: 'Learning to Write as a Professional Author',
               lessons: 20,
               students: 50,
            },
            {
               imgPath: require('../assets/img/stock-full-hd-03-480x298.jpg'),
               price: 'Free',
               caption: 'Customer-centric Info-Tech Strategies',
               lessons: 24,
               students: 769,
            },
            {
               imgPath: require('../assets/img/stock-full-hd-04-480x298.jpg'),
               price: '19',
               caption: 'Oper programming Courses for Everyone: Python',
               lessons: 17,
               students: 62,
            },
            {
               imgPath: require('../assets/img/stock-full-hd-06-480x298.jpg'),
               price: '26',
               caption: 'Academic Listening and Note-taking',
               lessons: 14,
               students: 67,
            },
            {
               imgPath: require('../assets/img/course-featured-image-01-480x298.jpg'),
               price: '39',
               caption: 'Master jQuery in a Short Period of Time',
               lessons: 6,
               students: 51,
            },
            {
               imgPath: require('../assets/img/stock-full-hd-05-480x298.jpg'),
               price: '59',
               caption: 'Introduction to Javascript for Beginners',
               lessons: 14,
               students: 76,
            },
         ],
         clients: [
            require('../assets/img/client-logo-colored-01.png'),
            require('../assets/img/client-logo-colored-02.png'),
            require('../assets/img/client-logo-colored-03.png'),
            require('../assets/img/client-logo-colored-04.png'),
            require('../assets/img/client-logo-colored-05.png'),
            require('../assets/img/client-logo-colored-06.png'),
         ],
         articles: [
            {
               artist: 'artist',
               imgPath: require('../assets/img/artist-blog-03-480x325.jpeg'),
               title: 'Brush Strokes Energize Trees in Paintings',
               date: 'May, 15, 2020',
               views: 688,
            },
            {
               artist: 'artist',
               imgPath: require('../assets/img/artist-blog-01-480x325.jpg'),
               title: 'Pocket-Sized Notebooks Hold Miniature Paintings',
               date: 'May, 15, 2020',
               views: 603,
            },
            {
               artist: 'artist',
               imgPath: require('../assets/img/artist-blog-02-480x325.jpg'),
               title: 'Connection Between Self-Portraits and Identiy',
               date: 'May, 15, 2020',
               views: 397,
            },
         ]
      }
   }
}
</script>

<style lang="scss">

@import '../assets/style/mixins.scss';


</style>