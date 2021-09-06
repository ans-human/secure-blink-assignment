<template>
  <section class="top-earners">
      <p class="sec">Top Earners</p>
      <h1>Transforming Your Ideas Into Reality</h1>
      <ul>
          <li v-for="earner in earners" :key="earner.image">
              <!-- <img src="@/assets/e1.png"/> -->
              <img :src="require('@/assets/' + earner.image + '')"/>
              <div class="earning">
                  <img src="@/assets/earn_rectangle.svg"/>
                  <p> {{earner.earning}}</p>
              </div>
          </li>
      </ul>
  </section>
</template>

<script>
export default {
    name: 'TopEarners',
    data(){
        return{
            earners: [
                { image: 'e1.png', earning:'₹8,00,000'},
                { image: 'e2.png', earning:'₹6,00,000'},
                { image: 'e3.png', earning:'₹5,00,000'},
                { image: 'e4.png', earning:'₹4,50,000'},
            ]
        }
    }
}
</script>

<style scoped>
    *{
        margin: 0;
        padding: 0;
    }
    section h1{
        width:100%;
        padding: 1rem 0;
    }
    section {
        text-align: left;
        margin: 2rem;
    }
    section .sec{
        color: #01CB63;
        font-style: italic;
    }
    ul {
        display: grid;
        grid-template-rows: 1fr 1fr;
        grid-template-columns: 1fr 1fr;
        list-style: none;
        max-height: 100%;
        justify-content: space-around;
    }
    li {
        padding-right: 2.5rem;
        align-items: left;
        padding-bottom: 1rem;
    }   
    img {
        object-fit: cover;
        max-height: 100%;
        max-width: 100%;
    }
    .earning {
        align-items: center;
        font-weight: bold;
        font-size: 1.2rem;
        display: flex;
    }
    .earning img {
        padding-right:.5rem;
        height: 2.5rem;
        width: .5rem;
    }
    @media(min-width: 768px){
        section h1{
            width:50%;
            padding: 1 2rem 0;
        }
        section{
            margin-left: 4rem;
            margin-left: 4rem;
        }
        ul {
            list-style: none;
            display: flex;
            max-height: 100%;
            justify-content: space-around;
        }
    }
    @media(min-width: 1020px){
        section{
            margin-left: 6rem;
            margin-right: 6rem;
        }
        section h1{
            width:30%;
        }
    }
</style>