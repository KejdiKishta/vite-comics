<script>
export default {
    data() {
        return {
            navList: [
                {
                    icon:"buy-comics-digital-comics.png",
                    name:"DIGITAL COMICS",
                },
                {
                    icon:"buy-comics-merchandise.png",
                    name:"DC MERCHANDISE",
                },
                {
                    icon:"buy-comics-subscriptions.png",
                    name:"SUBSCRIPTION",
                },
                {
                    icon:"buy-comics-shop-locator.png",
                    name:"COMIC SHOP LOCATOR",
                },
                {
                    icon:"buy-dc-power-visa.svg",
                    name:"DC POWER VISA",
                },
            ]
        }
    },
    methods: {
        getImagePath: function(image) {
            return new URL(`../assets/img/${image}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <nav>
        <ul class="container">
            <li v-for="item in navList">
                <img :src="getImagePath(item.icon)">
                <div>{{ item.name }}</div>
            </li>
        </ul>
    </nav>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixin" as *;

    nav {
        background-color: $blue-color;
        padding: 50px 0;
        color: $white-color;

        ul {
            list-style-type: none;
            @include flex (row, center, center);
            gap: 20px;
        }

        li {
            @include flex (row, center, center);
            height: 50px;
            gap: 10px;
        }

        li:last-child {
            img {
                width: 50%;
            }
        }

    }
</style>