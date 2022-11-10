<template>
   <section>
    <div class="container">
        <div class="links-list">
            <div>
                <h4>Dc Comics</h4>
                <ul>
                    <li>
                        <a href="#">Characters</a>
                    </li>
                    <li>
                        <a href="#">Comics</a>
                    </li>
                    <li>
                        <a href="#">Movies</a>
                    </li>
                    <li>
                        <a href="#">TV</a>
                    </li>
                    <li>
                        <a href="#">Games</a>
                    </li>
                    <li>
                        <a href="#">Videos</a>
                    </li>
                    <li>
                        <a href="#">New</a>
                    </li>
                </ul>
                <h4>Dc Comics</h4>
                <ul>
                    <li>
                        <a href="#">Shop DC</a>
                    </li>
                    <li>
                        <a href="#">Shop DC Collectables</a>
                    </li>
                </ul>
            </div>
            <div>
                <h4>Dc</h4>
                <ul>
                    <li>
                        <a href="#">Terms Of Use</a>
                    </li>
                    <li>
                        <a href="#">Privacy policy</a>
                    </li>
                    <li>
                        <a href="#">Ad Choices</a>
                    </li>
                    <li>
                        <a href="#">Advertising</a>
                    </li>
                    <li>
                        <a href="#">Jobs</a>
                    </li>
                    <li>
                        <a href="#">Subscriptions</a>
                    </li>
                    <li>
                        <a href="#">Talent Workshops</a>
                    </li>
                    <li>
                        <a href="#">CPSC Certificates</a>
                    </li>
                    <li>
                        <a href="#">Rating</a>
                    </li>
                    <li>
                        <a href="#">Shop Help</a>
                    </li>
                    <li>
                        <a href="#">Cntact Us</a>
                    </li>
                </ul>
            </div>
            <div>
                <h4>Sites</h4>
                <ul>
                    <li>
                        <a href="#">DC</a>
                    </li>
                    <li>
                        <a href="#">MAD Magazine</a>
                    </li>
                    <li>
                        <a href="#">DC Kids</a>
                    </li>
                    <li>
                        <a href="#">DC Universe</a>
                    </li>
                    <li>
                        <a href="#">DC Power Visa</a>
                    </li>
                </ul>
            </div>
        </div>
        <img src="../assets/img/dc-logo-bg.png" alt="dc logo">
    </div>
   </section>
</template>

<script>
    export default {
        name: 'LinkSectionComponent',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

section {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    overflow: hidden;

    .container {
        height: 420px;
        @include dflex;

        .links-list {
            display: flex;
            justify-content: space-between;
            align-self: flex-start;
            gap: 3rem;

            h4 {
                color: white;
                text-transform: uppercase;
                padding: 1rem 0;
                font-weight: bold;
                font-size: 1.2rem;
            }
            ul {
                list-style: none;
            }
            li {
                padding:0.3rem 0;
                font-size: 0.8rem;
                
                & a {
                    text-decoration: none;
                    color: gray;
                }
            }
        }
    }
}



</style>