<template>
    <div>
        <div class="navDiv">
            <button class="openSideNav" @click="showNav"><font-awesome-icon :icon="['fab', 'arrow']"/></button>
            <div class="flex"><p>Account Settings</p></div>
            <div><input type="search" placeholder="Search" class="input"></div>
        </div>
        <div class="midDiv"></div>
    </div>
</template>

<script>
    export default {
        methods: {
            showNav() {
                document.querySelector(".sideNav").style.width = "248px";
                document.querySelector('.main-content').style.marginLeft = "248px";
                document.querySelector('.openSideNav').style.display = 'none';
            },
        },
    }
</script>

<style lang="scss" scoped>

</style>