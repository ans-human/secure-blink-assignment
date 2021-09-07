<template>
    <footer>
        <div class="container">
            <a href="#"><p>2021-2022 &#169; Course Pro Private Limited</p></a>
        </div>
        <div class="container">
            <a href="#"><p>Terms &amp; Conditions</p></a>
            <a href="#"><p>Privacy Policy</p></a>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style scoped>
    a{
        text-decoration: none;
        color: inherit;
    }
    p{
        font-weight: bold;
    }
    @media(min-width: 768px) {
        footer{
            display: flex;
            justify-content: space-between;
            margin: 1rem 6rem;
        }
        .container{
            /* border: 2px solid black; */
            display: flex;
            justify-content: space-around;
        }
        p{
            padding-right: 2rem;
        }
    }
</style>