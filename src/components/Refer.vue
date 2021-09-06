<template>
  <section>
      <p>Refer</p>
      <h1>How It's Work</h1>
      <img src="@/assets/map.svg"/>
  </section>
</template>

<script>
export default {
    name: 'Refer',
}
</script>

<style scoped>
    section {
        text-align: left;
    }
    section h1, p{
        margin: 0 2rem;
    }
    section p{
        margin-top: 1rem;
        color: #01CB63;
        font-style: italic;
    }
    section img {
        max-width: 90vw;
        max-height: 90vh;
    }
    @media(min-width: 768px) {
        section h1,p {
            margin: auto 4rem;
        }
        secion {
            margin: 4rem;
        }
    }
    @media(min-width: 1020px) {
        section h1,p {
            margin: auto 6rem;
        }
        section p{
            margin-top: 6rem;
        }
    }
</style>