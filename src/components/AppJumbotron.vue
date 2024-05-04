<script>
import ButtonProps from './buttonProps.vue';

export default {
    components: {
        ButtonProps,
    },
    data() {
        return {
            btn: "CURRENT SERIES"
        }
    }
}
</script>

<template>
    <div>
        <buttonProps :text="btn" />
    </div>
</template>

<style scoped lang="scss">
    div {
        position: relative;
        height: 50vh;
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: cover;

        button {
            position: absolute;
            bottom: -20px;
            left: 15%;
        }
    }
</style>