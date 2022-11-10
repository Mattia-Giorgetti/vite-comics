<template>
   <footer>
    <div class="container">
        <div class="foot_left">
            <button>Sign-up now!</button>
        </div>
        <div class="foot_right">
            <span>
                <a href="#">Follow Us</a>
            </span>
            <img src="../assets/img/footer-facebook.png" alt="fb logo">
            <img src="../assets/img/footer-twitter.png" alt="twitter logo">
            <img src="../assets/img/footer-youtube.png" alt="YT logo">
            <img src="../assets/img/footer-pinterest.png" alt="Pinterest logo">
            <img src="../assets/img/footer-periscope.png" alt="map logo">
        
        </div>
    </div>
   </footer>
</template>

<script>
    export default {
        name:'FooterComponent',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

footer {
    background-color: $darkgray;
    .container {
        @include dflex;
        height: 120px;
        button {
            border: 2px solid $blue;
            padding: .8rem 1.2rem;
            background-color: $darkgray;
            font-size: 1rem;
            font-weight: 600;
            text-transform: uppercase;
            color: white;
            cursor: pointer;
            transition: all 0.3s ease;

            &:hover {
                background-color: $blue;
            }
        }
        & .foot_right {
            @include dflex;
            gap: 1rem;

            img {
                transition: all 0.5s ease;
            }
            span a {
                color: $blue;
                display: block;
                text-decoration: none;
                text-transform: uppercase;
                font-size: 1.2rem;
                font-weight: 600;
                margin-right: 1.2rem;
                transition: color 0.3s linear;

                &:hover {
                    color: white;
                }
            }
            img:hover {
                transform: translateY(- 0.5rem);
                cursor: pointer;
            }
        }
    }
}

</style>