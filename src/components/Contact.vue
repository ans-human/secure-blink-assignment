<template>
<p class="sec">Contact Us</p>
      <h1>Reach Out With Any Question You Have</h1>
  <section>
      
      <MessageForm class="form"/>
      <div class="contact-info">
          <ul>
            <li><h3>Contact Information</h3></li>
            <li class="info">
                <img src="@/assets/mail.svg">
                <p>contact@coursepro.com</p>
            </li>
            <li class="info">
                <img src="@/assets/call.svg">
                <p>1800-562-895, 1800-869-877</p>
            </li>
            <li class="info">
                <img src="@/assets/location.svg">
                <p>102 Street, India</p>
            </li>
          </ul>
      </div>
      <div class="social">
          <h3>Social Media Channel</h3>
          <img src="@/assets/Facebook.svg" />
          <img src="@/assets/Twitter.svg" />
          <img src="@/assets/Github.svg" />
          <img src="@/assets/Linkedin.svg" />
      </div>
  </section>
</template>

<script>
import MessageForm from './MessageForm.vue'
export default {
    name: 'Contact',
    components: {
        MessageForm,
    },
}
</script>

<style scoped>
    *{
        margin: 0;
        padding: 0;
        max-width: 100%;
    }
    ul {
        /* text-align: left; */
        list-style: none;
        width: 100%; 
	    margin-left: auto; 
	    margin-right: auto; 
        display: inline-block;
    }
    li {
        /* margin: 0 1rem; */
    }
    .sec{
        margin-top: 1rem;
        color: #01CB63;
        font-style: italic;
    }
    section{
        /* border: 2px solid red; */
        /* margin: 2rem; */
        background-color: #F8F9FB;
    }
    section h1{
        margin: 0 2rem;
    }
    .info p{
        font-weight: bold;
        color: #201F23;
    }
    .info {
        display: flex;
        align-items: center;
        /* justify-content: center; */
    }
    .info img{
        height: 4em;
    }
    .social{
        margin: 2rem 0;
    }
    .social img{
        height: 2.5rem;
        margin: 1rem;
    }
    
    @media(min-width: 768px) {
        section{
            /* border: 2px solid red; */
            /* margin: 6rem; */
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            grid-template-rows: repeat(12,1fr); 
            /* grid-area: 
                "contact form form"
                "contact form form"
                "social form form"; */
            
        }
        .contact-info{
            /* grid-area: contact; */
            text-align: left;
            margin: 6rem;
            grid-column: 1 / span 6;
            grid-row: 1 / span 8;
        }
        .form{
            /* grid-area: form; */
            grid-column: 6 / span 12;
            grid-row: 1 / span 12;
        }
        .social {
            margin-left: 6rem;
            text-align: left;
            /* grid-area: social; */
            grid-column: 1 / span 4;
            grid-row: 8 / span 12;
        }
    }
    @media(min-width: 1200px){
        
    }
</style>