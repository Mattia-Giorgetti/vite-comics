<template>
    <div class="mycol">
        <div class="img_wrapper"><img :src="object.thumb" :alt="object.series"></div>
        <h4>{{object.series}}</h4>
    </div>
</template>

<script>

    export default {
        name: 'CardComponent',
        props: ['object']
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

img {
    transition: all 0.3s ease;
}
.img_wrapper {
    width: 100%;
    height: 157px;
    overflow: hidden;

    &:hover img {
        transform: scale(1.2);
    }
}
h4 {
    color: white;
    text-transform: uppercase;
    font-weight: 500;
    font-size: 0.8rem;
    margin-top: 0.6rem;

    &:hover {
        text-decoration: underline;
        cursor: pointer;
    }
}

</style>