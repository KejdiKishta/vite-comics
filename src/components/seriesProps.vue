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
        padding: 5px;
        margin-bottom: 10px;

        &:hover {
            background-color: $white-color;
            cursor: pointer;

            h5 {
                color: $black-color;
            }
        }

        img {
            width: 100%;
            aspect-ratio: 0.7;
        }

        h5 {
            color: $white-color;
            font-size: .8rem;
            height: 40px;
            margin: 15px 0;
        }
    }

</style>