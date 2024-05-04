<script>
export default {
    props: {
        text: String,
    },
    data() {
        return {
        }
    }
}
</script>

<template>
    <button>{{ text }}</button>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;

button {
            @include button (10px, rgb(2 130 249), white, none);
            font-weight: bold;
            cursor: pointer;
        }
</style>