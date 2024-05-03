<script>
export default {
    data() {
        return {
            headerNav: [
                {
                    item: "CHARACTER",
                    isActive: false
                },
                {
                    item: "COMICS",
                    isActive: true
                },
                {
                    item: "MOVIES",
                    isActive: false
                },
                {
                    item: "TV",
                    isActive: false
                },
                {
                    item: "GAMES",
                    isActive: false
                },
                {
                    item: "COLLECTIBLES",
                    isActive: false
                },
                {
                    item: "VIDEOS",
                    isActive: false
                },
                {
                    item: "FANS",
                    isActive: false
                },
                {
                    item: "NEWS",
                    isActive: false
                },
                {
                    item: "SHOP",
                    isActive: false
                }
            ]
        }
    }
}
</script>

<template>
    <header class="container">
        <div><img src="../assets/img/dc-logo.png" alt=""></div>
        <ul>
            <li v-for="link in headerNav">
                <a href="#" :class="{'active': link.isActive}">{{ link.item }}</a>
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
    }

</style>