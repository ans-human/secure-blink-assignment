<template>
  <div class="course">
      <img :src="require('@/assets/' + card.img + '')"/>
      <div class="details">
          <h3 class="title">{{card.title}}</h3>
          <small class="students"><b>{{card.noStudents}}</b> Student</small>
          <div class="time">
              <div class="hours">
                <img src="@/assets/schedule-24px.svg"/>
                <p> {{card.hours}} hrs {{card.minutes}} min</p>
              </div>
              <div class="hours">
                <img src="@/assets/date_range-24px.svg"/>
                <p>{{card.noLectures}} Lectures</p>
              </div>  
          </div>
          <div class="author">
              <p>{{card.author}}</p>
              <div class="price">
                  <p>{{card.price}}</p>
                  <small class=""> <del>{{card.price}}</del></small>
              </div>
              
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'CourseCard',
    data(){
        console.log(this.card)
        return{
            image: '@/assets/' + this.card.img, 
        }
    },
    props: {
        card: Object,
    },
}
</script>

<style scoped>
    * {
        margin: 0;
        padding: 0;
    }
    .course {
        max-height: 100%;
        border: 1px solid #E6E6E6;
        border-radius: 1rem;
        text-align: left;
        display: grid;
        grid-template-rows: 1fr auto ;
    }
    img {
        border-radius: 1rem 1rem 0rem 0rem;
        padding: 0;
        margin: 0;
        /* object-fit: cover; */
        max-height: 100%;
        max-width: 100%;
    }
    .details {
        padding: 1rem;
        display: grid;
        grid-template-rows: 1fr auto auto auto;
        grid-template-areas:
            "title"
            "students"
            "time"
            "author";
        max-height: 100%;
        grid-gap: 1rem;
    }
    .time {
        font-style: italic;
        color: #86919D;
        grid-area: time;
        display: flex;
        justify-content: space-between;
        border-bottom: 1px solid #E6E6E6;
    }
    .author{
        font-weight: bold;
        grid-area: author;
        display: flex;
        justify-content: space-between;
    }
    .title{
        grid-area: title;
    }
    .students{
        font-style: italic;
        grid-area: students;
    }
    .hours{
        display: flex;
        font-size: small;
    }
    .hours img{
        height: 80%;
    }
    .price {
        display: flex;
        align-items: flex-end;
    }
    .price p{
        color: #01CB63;
    }
</style>