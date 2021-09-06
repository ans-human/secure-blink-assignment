<template>
  <Navbar/>
  <Hero/>
  <Courses/>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Courses from './components/Courses.vue'
export default {
  name: 'App',
  components: {
    Navbar,
    Hero,
    Courses,
  }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Noto+Sans:ital,wght@0,400;0,700;1,400;1,700&display=swap');
#app {
  font-family: Noto Sans, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: #FFFFFF 0% 0% no-repeat padding-box;
  margin: 0;
  padding: 0;
}
</style>
