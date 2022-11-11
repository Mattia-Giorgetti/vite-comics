<template>
   <section>
   <div class="container">
        <div class="current_series">
            <h2>Current Series</h2>
        </div>
   </div>

   </section>
</template>

<script>
    export default {
        name: 'JumboComponent'
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

section{
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    height: 380px;
    
    .container {
        height: 100%;
        position: relative;
    }
    .current_series {
        background-color: $blue;
        display: inline-block;
        padding: 0.7rem 1.8rem;
        color: white;
        text-transform: uppercase;
        font-size: 0.8rem;
        position: absolute;
        left: 1rem;
        bottom: -25px;
    }
}
</style>