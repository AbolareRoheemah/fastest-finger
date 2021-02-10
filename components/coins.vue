<template>
    <div>
        <AddModal />
        <EditCoin />
        <div class="coins-mid">
            <table class="paddi">
                <thead class="top-band">
                    <th class="thead-data">Coin Quantity</th>
                    <th class="thead-data">Quantity</th>
                    <th class="thead-data">Price</th>
                    <th class="thead-data">Date Created</th>
                    <th class="thead-data">Action</th>
                    <th class="thead-data">Expiry</th>
                </thead>
            <NuxtChild />
            </table>
            <div class="smallBoxes">
                <nuxt-link to= "/Coins/first-page" id="prev_btn"><div class="boxes"><font-awesome-icon :icon="['fas', 'chevron-left']"/></div></nuxt-link>
                <div class="boxes">1</div>
                <p>...</p>
                <div class="boxes">4</div>
                <div class="boxes">5</div>
                <div class="boxes">6</div>
                <div class="boxes">7</div>
                <div class="boxes">8</div>
                <p>...</p>
                <div class="boxes">50</div>
                <nuxt-link to= "/Coins/last-page" id="nxt_btn"><div class="boxes"><font-awesome-icon :icon="['fas', 'chevron-right']"/></div></nuxt-link>
                <div>Go to</div>
                <div class="goto" role="input"></div>
            </div>
            <!-- <span id="page"></span> -->
        </div>
        <div class="marginTest"></div>
    </div>
</template>

<script>
import AddModal from '~/components/new-coins-modal.vue';
import EditCoin from '~/components/editCoins.vue';
    export default {
        components: {
            AddModal,
            EditCoin,
        },
         methods: {
            closeModal() {
                let modalBtn = document.querySelector('#modal-btn');
                let modal = document.querySelector('.modal');
                let closeBtn = document.querySelector('.close-btn');
                modal.style.display = 'none';
            },  
            showModal1() {
                let modalBtn1 = document.querySelector('.pen');
                let modal1 = document.querySelector('.modal1');
                let closeBtn1 = document.querySelector('.close-btn1');
                modal1.style.display = 'block';
            },
            deleteCoin() {
                const oneCoin = document.querySelector('.next-band');
                oneCoin.remove();
            },
        },
        mounted () {
            let modalBtn = document.querySelector('#modal-btn');
            modalBtn.style.display = 'block';
        }
    }
</script>