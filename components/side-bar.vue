<template>
    <div>
        <nav class="sideNav">
        <span>Fastest Finger</span> <a href="#" class="closeBtn" @click="hideNav"> <img src="img/fastestArrow.png" class="arrow" alt=""></a>
        <hr class="Hr">
        <a href="#">Menu</a>
        <a href="#">Dashboard</a>
        <a href="#">Contests</a>
        <a href="#">Users</a>
        <a href="#">Adverts</a>
        <a href="#">Coins Pricing</a>
        <a href="#">Account Settings</a>
        </nav>
        <main class="main-content">
        
        
        <!-- <div class="navDiv">
            <button class="openSideNav"><img src="img/arrowIcon.png" alt=""></button>
            <div class="flex"><p>Account Settings</p></div>
            <div><input type="search" placeholder="Search" class="input"></div>
        </div>
        <div class="midDiv"></div> -->
        </main>
    </div>
</template>

<script>


export default {
    methods: {
        hideNav() {
            document.querySelector(".sideNav").style.width = "0";
            document.querySelector('.main-content').style.marginLeft = "0px";
            document.querySelector('.openSideNav').style.display = 'block';
        }
    },   
}
</script>



<style lang="scss" scoped>

</style>