<template>
  <div class="navbar">
    <nav>
      <img src="@/assets/course_pro_logo.svg"/>
      <div class="links">
        <button @click="handleClick" class="secondary">Login</button>
        <button @click="handleClick" class="primary">Register</button>
      </div>
    </nav>
  </div>
</template>

<script>

export default {
  name: 'Navbar',
}
</script>

<style scoped> 
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans&display=swap');
  .navbar {
    padding: 16px 10px;
    background: white;
  }
  nav {
    display: flex;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
  }
  nav img {
    max-height: 60px;
  }
  nav h1 {
    margin-left: 20px;
  }
  nav .links {
    margin-left: auto;
  }
  nav .links a, button {
    margin-left: 16px;
    font-size: 14px;
  }
  button {
    box-sizing: border-box;
    font-family: Noto Sans;
    border: none;
    padding: .8rem;
    border-radius: .5rem;
    cursor: pointer;
    letter-spacing: 1px;
  }
  .primary{
    background-color: #01CB63;
    box-shadow: 0px 1px 5px #848d88;
    font-style: italic;
    color: white;
  } 
  .secondary{
    font-weight: bold;
    background: none;
  }
  svg {
    font-family: Noto Sans, sans-serif;
  }
</style>