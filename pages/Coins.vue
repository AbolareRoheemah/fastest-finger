<template>
    <div>
        <Coins />
    </div>
</template>

<script>
import Coins from "~/components/coins.vue";
    export default {
        name: 'CoinsPa',
        components: { Coins },
        mounted () {
            this.names = this.$nuxt.$route.name;
        },
    }
</script>

<style lang="scss" scoped>

</style>