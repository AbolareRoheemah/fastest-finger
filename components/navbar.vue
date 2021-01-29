<template>
    <div class="main-content">
        <div class="navDiv">
            <a class="openSideNav" @click="showNav"><font-awesome-icon :icon="['fas', 'chevron-circle-right']"/></a>
            <div class="flex"><p>Account Settings</p></div>
            <div class="inputParent"><input type="search" placeholder="Search `<font-awesome-icon :icon='['fas', 'search']'/>`" class="input"></div>
            <p class="helloText">Hello, Precious</p>
            <img src="~/assets/img/image 1.png" alt=""><a href="#"><font-awesome-icon :icon="['fas', 'sort-down']"/></a>
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