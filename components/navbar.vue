<template>
    <div class="main-content">
        <div class="navDiv">
            <a class="openSideNav" @click="showNav"><font-awesome-icon :icon="['fas', 'chevron-circle-right']"/></a>
            <div class="flex"><nuxt-link to='/CoinsPage'><p class="Navname">Account Settings</p><div class="button" id="modal-btn" @click="showModal" role="button">New Pricing</div></nuxt-link></div>
            <div class="input" role="input"><span>Search</span><a class="searchIcon"><font-awesome-icon :icon="['fas', 'search']"/></a></div>
            <p class="helloText">Hello, Precious</p>
            <img src="~/assets/img/image 1.png" alt=""><a href="#" class="picIcon"><font-awesome-icon :icon="['fas', 'sort-down']"/></a>
        </div>
        <!-- <input type="search" placeholder="Search" class="input"> -->
    </div>
</template>

<script>
    export default {
        methods: {
            showNav() {
                document.querySelector(".sideNav").style.width = "248px";
                document.querySelector('.main-content').style.marginLeft = "248px";
                document.querySelector('.openSideNav').style.display = 'none';
                document.querySelector('.searchIcon').style.right = '20%';
            },
            showModal() {
                let modalBtn = document.querySelector('#modal-btn');
                let modal = document.querySelector('.modal');
                let closeBtn = document.querySelector('.close-btn');
                modal.style.display = 'block';
            },
        },
        mounted () {
            document.querySelector('#modal-btn').style.display = 'none';
        },
    }
</script>

<style scoped>
.Navname {
    color: #000000;
}
</style>