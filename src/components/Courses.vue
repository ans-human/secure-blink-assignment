<template>
  <section class="section">
      <p>Courses</p>
      <h1>Our Most Popular Courses</h1>
      <ul id="array-rendering">
        <li v-for="card in cards" :key="card.title">
            <course-card :card="card"></course-card>
        </li>
      </ul>
  </section>

</template>

<script>
import CourseCard from './CourseCard.vue'
export default {
    name: 'Courses',
    data(){
        return {
            cards: [
                {   
                    img: 'wes-hicks.jpg',
                    title: 'Ultimate Business Intelligence Analyst A to Z Course 2021' ,
                    noStudents: '46,995',
                    noLectures: '44',
                    hours: '11',
                    minutes: '20',
                    author: 'Albert Hitler',
                    price: '₹2000',
                },
                {
                    img: 'ui-design.jpg',
                    title: 'Adobe Photoshop Training: From Beginner to Pro' ,
                    noStudents: '6,995',
                    noLectures: '24',
                    hours: '6',
                    minutes: '20',
                    author: 'Wanda Wilson',
                    price: '₹3000',
                },
                {
                    img: 'social-media.jpg',
                    title: 'Social Media Marketing - A to Z Content Marketing class 2021' ,
                    noStudents: '46,995',
                    noLectures: '44',
                    hours: '11',
                    minutes: '20',
                    author: 'Albert Hitler',
                    price: '₹2000',
                },
            ]
        }
    },
    components: {
        CourseCard
  }
}
</script>

<style scoped>
    *{
        margin: 0;
        padding: 0;
    }
    .section{
        padding: 4rem 0rem;
        justify-content: center;
    }
    .section p{
        font-style: italic;
        color: #01CB63;
    }
    .section h1{
        font-weight: bold;
        font-size: 2rem;
    }
    .section ul{
        list-style: none;
        /* display: grid; */
        /* grid-template-rows: 1fr 1fr 1fr; */
    }
    .section li{
        margin: 1rem;
        justify-items: center;
    }
    .section course-card{
        object-fit: cover;
        max-width: 300px;
    }
    @media (min-width: 768px){
        .section ul{
            /* display: grid;
            grid-template-columns: 1fr 1fr 1fr; */
        }
    }

</style>