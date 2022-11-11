<template>
    <section>
        <div class="container">
            <div class="myrow">
                <CardComponent v-for="(item, index) in comicsList" :key="index" :object="item" />
            </div>
            <button>Load More</button>
        </div>
    </section>
</template>

<script>
    import {comics} from '../data/datas.js';
    import CardComponent from './CardComponent.vue';
    export default {
        name: 'ContentSectionComponent',
        components: {CardComponent},
        data() {
            return {
                comicsList: comics, 
            }
        },
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

section {
    background-color: black;
    button {
        display: block;
        margin: 2rem auto;
        padding: 0.6rem 3.5rem;
        margin-bottom: 0.5rem;
        border: 1px solid $blue;
        background-color: $blue;
        color: white;
        text-transform: uppercase;
        font-size: 0.7rem;
        font-weight: 600;
        transition: all 0.3s ease;

        &:hover {
            background-color: black;
            border: 1px solid $blue;
            cursor: pointer;
        }
    }

    .myrow {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        padding-top: 1.5rem;

        .mycol {
            flex-basis: calc(100% / 6);
            padding: 1rem;
        }
    }
}

</style>