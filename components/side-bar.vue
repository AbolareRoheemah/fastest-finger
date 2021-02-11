<template>
    <div>
        <nav class="sideNav">
        <p>Fastest Finger</p> <a href="#" class="closeBtn" @click="hideNav"><font-awesome-icon :icon="['fas', 'chevron-left']"/></a>
        <hr class="Hr">
        <a href="#">Menu</a>
        <a href="#">Dashboard</a>
        <a href="#">Contests</a>
        <a href="#">Users</a>
        <a href="#">Adverts</a>
        <a href="#">Coins Pricing</a>
        <a href="#">Account Settings</a>
        </nav>
    </div>
</template>

<script>


export default {
    methods: {
        hideNav() {
            document.querySelector(".sideNav").style.width = "0";
            document.querySelector('.main-content').style.marginLeft = "0px";
            document.querySelector('.openSideNav').style.display = 'block';
            document.querySelector('.searchIcon').style.right = '27%';

        }
    },   
}
</script>



<style lang="scss" scoped>

</style>