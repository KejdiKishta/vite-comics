<script>
export default {
    data() {
        return {
            dcComicsNav: [
                "Character",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Videos",
                "News",
            ],
            shopNav: [
                "Shop Dc",
                "Shop Dc Collectibles"
            ],
            dcNav: [
                "Terms Of Use",
                "Privacy Policy (New)",
                "Ad Choises",
                "Advertising",
                "Jobs",
                "Subscriptions",
                "Talent Workshops",
                "CPSC Certificates",
                "Ratings",
                "Shop Help",
                "Contact Us"
            ],
            sitesNav: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa"
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="overlay container">
            <nav>
                <div>
                    <h3>DC COMICS</h3>
                    <ul>
                        <li v-for="link in dcComicsNav">{{ link }}</li>
                    </ul>
                </div>
        
                <div>
                    <h3>SHOP</h3>
                    <ul>
                        <li v-for="link in shopNav">{{ link }}</li>
                    </ul>
                </div>
        
                <div>
                    <h3>DC</h3>
                    <ul>
                        <li v-for="link in dcNav">{{ link }}</li>
                    </ul>
                </div>
        
                <div>
                    <h3>SITES</h3>
                    <ul>
                        <li v-for="link in sitesNav">{{ link }}</li>
                    </ul>
                </div>
            </nav>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    section {
        background-image: url(../assets/img/footer-bg.jpg);

        .overlay {
            background-image: url(../assets/img/dc-logo-bg.png);
            background-repeat: no-repeat;
            background-position: right;
            background-size: 450px
        }
    }

    nav {
        @include flex (column, normal, flex-start);
        height: 300px;
        flex-wrap: wrap;
        width: 50%;
        font-size: .8rem;

        h3 {
            color: $white-color;
            padding: 15px 0;
        }

        ul {
            list-style-type: none;

            li {
                color:rgb(124 132 131);
                padding: 3px;
            }
        }
    }
</style>