<template>
  <form @submit.prevent="handleSubmit">
    <p>Fill up the form and our team will get back to you within 24 hours</p>
    <input type="name" placeholder="Name" v-model="name" required>
    <!-- <div v-if="nameError" class="error">{{ nameError }}</div> -->
    
    <input type="email" placeholder="Email" v-model="email" required>
    <!-- <div v-if="nameError" class="error">{{ nameError }}</div> -->

    <input type="phone" placeholder="Phone" v-model="phone" required>
    <div v-if="phoneError" class="error">{{ phoneError }}</div>
    
    <input type="subject" placeholder="Subject" v-model="subject" required>
    <!-- <div v-if="passwordError" class="error">{{ passwordError }}</div> -->

    <input type="message" placeholder="Message" v-model="message" required>

    <div class="submit">
      <button>Submit</button>
    </div>
  </form>
</template>

<script scoped>
export default {
    name: 'MessageForm',
    data() {
    return {
      name: '',
      email: '',
      phone: '',
      subject: '',
      message: '',
    }
  },
  methods: {
    handleSubmit() {
      // validate password
      this.passwordError = this.password.length > 5 ?
        '' : 'Password must be at least 6 characters long'
      if (!this.passwordError) {
        // make request to database to save user
        console.log('email: ', this.email)
        console.log('password: ', this.password)
        console.log('role: ', this.role)
        console.log('skills: ', this.skills)
        console.log('terms accepted: ', this.terms)
      }
    }
  }
}
</script>

<style scoped>
    form{
        background: #F8F9FB;
        padding: 1rem;
        text-align: center;
        align-items: center;
    }
    form p{
        font-weight: bold;
    }
    input, select {
        background-color: #F8F9FB;
        font-family: Noto Sans, sans-serif;
        font-style: italic;
        align-items: center;
        display: inline-block;
        padding: .5rem;
        margin: 1rem;
        width: 80%;
        justify-content: center;
        box-sizing: border-box;
        border: none;
        border-bottom: 2px solid #01CB63;
        color: #86919D;
    }
    .error {
        color: #ff0062;
        margin-top: 10px;
        font-size: 0.8em;
        font-weight: bold;
    }
    .submit button{
        margin: 1rem;
        font-family: Noto Sans, sans-serif;
        font-style: italic;
        color: white;
        padding: .8rem 2rem;
        border: none;
        background: black;
        border-radius: 10px;
        /* width:2rem; */
    }
    :focus {
        outline: 0;
        outline-color: transparent;
        outline-style: none;
    }
    @media(min-width: 768px) {
        form{
            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-template-rows: repeat(5, 1fr);
        }
        input[type="name"]{
            grid-column: 1 ;
            grid-row: 2;
        }
        input[type="email"]{
            grid-column: 2 ;
            grid-row: 2;
        }
        input[type="phone"]{
            grid-column: 1;
            grid-row: 3;
        }
        input[type="subject"]{
            grid-column: 2;
            grid-row: 3;
        }
        input[type="message"]{
            grid-column: 1/ span 2;
            grid-row: 4;
        }
        .submit button{
            grid-column: 1/ span 2;
            grid-row: 5;
        }

    }
    
</style>