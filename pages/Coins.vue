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
        
        created () {
            if (this.checkName == 'index') {
                this.names = 'Account Settings';
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>