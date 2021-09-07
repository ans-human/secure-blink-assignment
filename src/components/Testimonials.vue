<template>
  <section>
      <p class="sec">Testimonials</p>
      <h1>Check out What Our Students Think About Us</h1>
      <div class="quotes">
          <ul>
              <li v-for="quote in quote" :key="quote.author">
                  <div class="quote">
                      <p>{{quote.q}}</p>
                  </div>
                  <div class="author">
                      <div class="user">
                          <div class="dp">
                            <img :src="require('@/assets/' + quote.image + '')"/>
                          </div>
                          <div class="user-time">
                            <p>{{quote.author}}</p>
                            <small>{{quote.time}}</small>
                          </div>
                      </div>
                      <img src="@/assets/right-quotation-sign.svg"/> 
                  </div>
              </li>
          </ul>
      </div>
  </section>
</template>

<script>
export default {
    name: 'Testimonials',
    data(){
        return{
            quote: [
                {
                    q : 'It\'s a comprehensive online learning platform for everyone looking to learn and course pro. provinding this platform which is very beneficial for practicals. Students can revise everything at home like dissection and slides',
                    author: 'Anshul Jain',
                    time: 'Yesterday',
                    image: 'e1.png'
                },
                {
                    q : 'It\'s a comprehensive online learning platform for everyone looking to learn and course pro. provinding this platform which is very beneficial for practicals. Students can revise everything at home like dissection and slides',
                    author: 'Rajkumar Jain',
                    time: 'Yesterday',
                    image: 'e2.png'
                }
            ]
        }
    }
}
</script>

<style scoped>
    * {
        margin: 0;
        padding: 0;
    }
    section {
        margin: 1rem 2rem;
        text-align: left;
    }
    .sec{
        margin-top: 1rem;
        color: #01CB63;
        font-style: italic;
    }
    ul {
        /* border: 2px solid red; */
        list-style: none;
        /* display: flex; */
    }
    li {
        /* border: 2px solid green; */
        margin: 1rem;
        padding: 1rem;
        max-width: 100%;
        box-shadow: 0px 20px 30px #1F25321A;
        border-radius: .7rem;
    }
    .author {
        padding: 1rem;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .user {
        align-items: center;
        display: flex;
        justify-content: left;
    }
    .user img {
        max-height: 3rem;
        border-radius: 1.5rem;
    }
    .quote{
        font-style: italic;
        padding: 1rem;
        opacity: 70%;
    }
    .author p{
        padding: 0 1rem;
        font-weight: bold;
    }
    .author small{
        padding: 0 1rem;
        color: #545D7A;
        font-style: italic;
    }
    @media(min-width: 768px) {
        section {
            margin: 4rem;
        }
        ul {
            display: flex;
        }
        h1 {
            width: 50%;
        }
    }
    @media(min-width: 1020px) {
        section {
            margin: 6rem;
        }
        ul {
            display: flex;
        }
        h1 {
            width: 30%;
        }
    }
</style>