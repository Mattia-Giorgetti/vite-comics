<template>
    <section>
    <div class="container icons_section">
        <div class="icon_item" v-for="(item, index) in slots" :key="index">
            <img :src="getImagePath(`../assets/${item.img}`)" :alt="item.text">
            <a :href="item.url">{{item.text}}</a>
        </div>
    </div>
    </section>
</template>

<script>
    export default {
        name: 'IconsSectionComponent',
        data() {
            return {
                slots: [{
                    text: 'Digital Comics',
                    url: '#',
                    img: '../assets/img/buy-comics-digital-comics.png'
                },
                {
                    text: 'Dc Merchandise',
                    url: '#',
                    img: '../assets/img/buy-comics-merchandise.png'
                },
                {
                    text: 'Subscription',
                    url: '#',
                    img: '../assets/img/buy-comics-subscriptions.png'
                },
                {
                    text: 'Comic shop locator',
                    url: '#',
                    img: '../assets/img/buy-comics-shop-locator.png'
                },
                {
                    text: 'Dc power visa',
                    url: '#',
                    img: '../assets/img/buy-dc-power-visa.svg'
                },
            ],
            }
        },
        methods: {
            getImagePath: function(imgPath) {
                return new URL(imgPath, import.meta.url).href;
            }
        },
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

section {
    background-color: $blue;
    .icons_section {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 2rem;
        height: 160px;
        .icon_item {
            @include dflex;
            
            & img {
                width: 40px;
            }
            & a {
                text-decoration: none;
                font-size: .7rem;
                text-transform: uppercase;
                font-weight: 600;
                color: white;
                padding: 0 1rem ;
            }
        }
    }
    
}

</style>