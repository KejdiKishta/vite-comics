<script>
export default {
    data() {
        return {
            headerNav: [
                "CHARACTER",
                "COMICS",
                "MOVIES",
                "TV",
                "GAMES",
                "COLLECTIBLES",
                "VIDEOS",
                "FANS",
                "NEWS",
                "SHOP"
            ],
            activeIndex: 2,
        }
    },
    methods: {
        changeActive: function (index) {
            this.activeIndex = index;
            console.log(this.activeIndex);
        }
    }
}
</script>

<template>
    <header class="container">
        <div><img src="../assets/img/dc-logo.png" alt=""></div>
        <ul>
            <li v-for="(link, index) in headerNav">
                <a href="#" :class="{'active': index === activeIndex}" @click="changeActive(index)">{{ link }}</a>
            </li>
        </ul>
    </header>
</template>

<style scoped lang="scss">
    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    header {
        @include flex (row, space-between, center);
        font-size: .8rem;
        padding: 20px 0;
        width: 90%;
        max-width: 1100px;
        margin: auto;

        img {
            max-height: 80px;
        }
    }
    
    ul {
        @include flex (row, center, center);
        list-style-type: none;
        gap: 10px;

        a {
            text-decoration: none;
            color: $black-color;
            padding: 20px 0;
        }
        
        .active {
            border-bottom: 3px solid $blue-color;
            color: $blue-color;
            font-weight: bold;
        }

        li:hover a{
            border-bottom: 3px solid $blue-color;
            color: $blue-color;
            font-weight: bold;
        }
    }

</style>