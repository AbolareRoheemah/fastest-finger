<template>
    <div class="main-content">
        <div class="navDiv">
            <a class="openSideNav" @click="showNav"><font-awesome-icon :icon="['fas', 'chevron-circle-right']"/></a>
            <div class="flex">
                <nuxt-link to='/Coins'><p class="Navname" v-if="this.$route.name == 'index'">{{ Acctname }}</p>
                <p class="Navname" v-if="this.$route.name != 'index'">{{ $route.name }}</p>
                    <div v-if="this.$route.name != 'index' " class="button" id="modal-btn" @click="showModal" role="button">New Pricing</div>
                </nuxt-link>
            </div>
                <input type="text" class="input" v-model="Search"><!-- <font-awesome-icon :icon="['fas', 'search']" class="searchIcon"/> -->
            <p class="helloText">Hello, Precious</p>
            <img src="~/assets/img/image 1.png" alt="" class="userImg"><a href="#" class="picIcon"><font-awesome-icon :icon="['fas', 'sort-down']"/></a>
        </div>


    </div>
</template>

<script>
    export default {
        data() {
            return {
                flag: undefined,
                Search: 'Search',
                Acctname: 'Account Settings',
                CoinsName: 'Coins'
            }
        },
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
        created () {
            // if (this.$route.name == 'index') {
            //     this.name = ;
            
            // }
            // if (this.$route.name == 'Coins-first-page' || this.$route.name == 'Coins-last-page') {
            //     this.name = 'Coins'
            // }
        },
    }
</script>

<style scoped>
.Navname {
    color: #000000;
}
</style>