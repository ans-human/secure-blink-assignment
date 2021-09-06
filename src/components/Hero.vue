<template>
  <div class="hero">
    <div class="text">
        <h1 class="big-text">
            Anytime, Anywhere Learn On Your Schedule From Any Device
        </h1>
        <p class="small-text">
            <i>We Believe everyone has the capcity to be creative <mark>Course Pro</mark> is a place where people develop their own potential.</i>
        </p>
        <a href="#"><button>Let's Get Start</button></a>
    </div>
    <img class="image" src="@/assets/biting_pencil.jpg"/>
  </div>
    <ul id="stats">
        <li>
            <p>Total Students</p>
            <h1>5140</h1>
        </li>
        <li>
            <p>Partners</p>
            <h1>4123</h1>
        </li>
        <li>
            <p>Affiliate Distributions</p>
            <h1>4.18 Lac</h1>
        </li>
    </ul>
</template>

<script>
export default {
    name: "Hero"
}
</script>

<style scoped>
    * {
        margin: 0;
        padding: 0;
    }
    ul{    
        list-style: none;
        background-image: url("~@/assets/dot_background.svg");
    }
    ul li{
        padding: 2rem;
        margin: 0 1rem;
        text-align: left;
    }
    ul li p{
        font-size: 1.5rem;
        font-weight: bold;
        color: gray;
    }
    ul li h1{
        border-bottom:5px solid #00D768;
        display: inline;
        font-size: 3rem;
    }
    .hero{
        text-align: left;
        background: #01CB63;
        display: grid;
        grid-template-rows: auto-fit 1fr 1fr;
        max-height: MediaQuery.of(context).size.width * 0.65;
        grid-area:   
            "image"
            "text";
        
    }
    
    .hero .text{
        grid-area: "text";
        padding: 2rem;
    }
    .hero .image{
        object-fit: cover;
        min-height: 100%;
        width: 100%;
        grid-area: "image";
        opacity: 65%;
        background: #00D768;
        background-image: linear-gradient(#01CB63, #00D768);
    }
    .hero .big-text{
        color: white;
    }
    .hero .text .small-text{
        margin-bottom: 2rem;
    }
    .hero .text .small-text mark{
        background: none;
        color: white;
        font-weight: bold;
        font-style: normal;
    }
    .hero .text button{
        font-family: Noto Sans, sans-serif;
        color: white;
        font-style: italic;
        background: black;
        padding: .8rem 2rem;
        border-radius: .5rem;
        border-style: none;
        cursor: pointer;
    }
    .hero .text button:hover{
        opacity: 80%;
    }
    @media (min-width: 768px) {
        .hero{
            grid-template-columns: 1fr 1fr;
            grid-area: "text" "image";
        }
         .hero .text{
            grid-area: "text";
            padding: 4rem;
            font-size: 1.2rem;
        }
        .hero .text button{
            font-size: 1.2rem;
        }
        ul{
        display: flex;
        align-items: stretch; /* Default */
        justify-content: space-evenly;
        width: 100%;
        list-style: none;
        text-align: center;
        /* justify-content: space-around; */
    }
    }
    @media (min-width: 1020px){
        .hero .text{
            padding: 6rem;
            font-size: 1.5rem;
        }
        li{
            display: inline;
        }
    }
</style>