<template>
   <section>
    <div class="container">
        <div class="links-list">
            <div>
                <h4>Dc Comics</h4>
                <ul>
                    <li v-for="(item, index) in comics" :key="index">
                        <a :href="item.url">{{item.linkText}}</a>
                    </li>
                </ul>
                <h4>Shop</h4>
                <ul>
                    <li v-for="(item,index) in shop" :key="index">
                        <a :href="item.url">{{item.linkText}}</a>
                    </li>
                </ul>
            </div>
            <div>
                <h4>Dc</h4>
                <ul>
                    <li v-for="(item, index) in dc" :key="index">
                        <a :href="item.url">{{item.linkText}}</a>
                    </li>
                </ul>
            </div>
            <div>
                <h4>Sites</h4>
                <ul>
                    <li v-for="(item, index) in sites" :key="index">
                        <a :href="item.url">{{item.linkText}}</a>
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
        data() {
            return {
                comics: [{
                    linkText: 'Characters',
                    url: '#' 
                },
                {
                    linkText: 'Comics',
                    url: '#' 
                },
                {
                    linkText: 'Movies',
                    url: '#' 
                },
                {
                    linkText: 'TV',
                    url: '#' 
                },
                {
                    linkText: 'Games',
                    url: '#' 
                },
                {
                    linkText: 'Videos',
                    url: '#' 
                },
                {
                    linkText: 'News',
                    url: '#' 
                }],
                shop: [
                    {
                    linkText: 'Shop DC',
                    url: '#' 
                },
                {
                    linkText: 'Shop DC Collectables',
                    url: '#' 
                },
                ],
                dc: [
                    {
                    linkText: 'Terms Of Use',
                    url: '#' 
                },
                {
                    linkText: 'Privacy Policy',
                    url: '#' 
                },
                {
                    linkText: 'Ad Choices',
                    url: '#' 
                },
                {
                    linkText: 'Advertising',
                    url: '#' 
                },
                {
                    linkText: 'Jobs',
                    url: '#' 
                },
                {
                    linkText: 'Subscriptions',
                    url: '#' 
                },
                {
                    linkText: 'Talent Workshops',
                    url: '#' 
                },
                {
                    linkText: 'CPSC Certificates',
                    url: '#' 
                },
                {
                    linkText: 'Ratings',
                    url: '#' 
                },
                {
                    linkText: 'Shop Help',
                    url: '#' 
                },
                {
                    linkText: 'Contact Us',
                    url: '#' 
                }
                ],
                sites: [
                    {
                    linkText: 'DC',
                    url: '#' 
                },
                {
                    linkText: 'MAD Magazine',
                    url: '#' 
                },
                {
                    linkText: 'DC Kids',
                    url: '#' 
                },
                {
                    linkText: 'DC Universe',
                    url: '#' 
                },
                {
                    linkText: 'DC Power Visa',
                    url: '#' 
                },
                ],
            }
        },
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
        height: 380px;
        @include dflex;
        img {
            margin-top: -8rem;
        }
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
                
                a {
                    text-decoration: none;
                    color: gray;

                    &:hover {
                        text-decoration: underline;
                    }
                }
            }
        }
    }
}



</style>