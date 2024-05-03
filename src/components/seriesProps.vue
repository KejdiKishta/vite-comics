<script>
export default {
    props: {
        cardThumb: String,
        cardPrice: String,
        cardSeries: String,
        cardType: String,
    },
    data() {
        return {
        }
    }
}
</script>

<template>
    <div class="card">
        <div>
            <img :src="cardThumb" :alt="cardSeries">
        </div>
        <h5>{{ cardSeries }}</h5>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    .card {
        width: 15%;

        img {
            height: 250px;
            width: 100%;
        }

        h5 {
            color:white;
            font-size: .8rem;
            height: 40px;
            margin: 15px 0;
        }
    }

</style>