<template>
    <header class="container">
        <img src="../assets/img/dc-logo.png" alt="dc logo">
        <nav>
            <ul>
                <li v-for="(item,index) in links" :key="index">
                 <a :href="item.url" :class="{'active' : item.current}">{{item.text}}</a>
                 <div class="underliner" :class="{'active' : item.current}"></div>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data(){
            return {
                links: [
                {
                    text: "Characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectables",
                    url: "#",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                },
            ],
            }
        },
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

header{
    @include dflex;
    img {
        width: 70px;
    }
    ul {
        @include dflex;
        list-style: none;

        li {
            position: relative;
        }

        li a {
            display: block;
            text-decoration: none;
            text-transform: uppercase;
            font-size: .7rem;
            padding: 1rem;
            font-weight: bold;
            color: $black;
            transition: all 0.3s ease;
            &:hover:not(.active) {
                color: gray;
            }
        }
    }
}
.underliner {
    background-color: $blue;
    height: 5px;
    width: 60%;
    position: absolute;
    left: 20%;
    bottom: - 1.8rem;
    opacity: 0;

    &.active {
        opacity: 1;
    }
}
.active {
    color: $blue;
}

</style>