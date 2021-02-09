<template>
    <div class="main-content">
        <div class="navDiv">
            <a class="openSideNav" @click="showNav"><font-awesome-icon :icon="['fas', 'chevron-circle-right']"/></a>
            <div class="flex">
                <nuxt-link to='/Coins/first-page'><p class="Navname">{{ names }}</p>
                    <div v-show="flag" class="button" id="modal-btn" @click="showModal" role="button">New Pricing</div>
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
                names: this.$nuxt.$route.name,
                Search: 'Search'
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
            if (this.names == 'index') {
                this.names = 'Account Settings';
            } else if (this.names == 'Coins' || this.names == 'Coins-last-page' || this.names == 'Coins-first-page') {
                this.names = 'Coins';
            }
        },
    }
</script>

<style scoped>
.Navname {
    color: #000000;
}
</style>