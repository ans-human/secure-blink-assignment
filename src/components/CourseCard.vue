<template>
  <div class="course">
      <div class="image">
          <h1>image</h1>
          <img src="@/assets/biting_pencil.jpg"/>
      </div>
      <div class="details">
          <h2>{{card.title}}</h2>
          <p>{{card.noStudents}} Student</p>
          <div class="time">
              <p>{{card.hours}} hrs {{card.minutes}} min</p>
              <p>{{card.noLectures}}</p>
          </div>
          <div class="author">
              <h3>{{card.author}}</h3>
              <h3>{{card.price}}</h3>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'CourseCard',
    props: {
        card: Object,
    }
}
</script>

<style>
    * {
        margin: 0;
        padding: 0;
    }
</style>