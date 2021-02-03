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
                <tr class="next-band">
                    <td class="thead-data">100</td>
                    <td class="thead-data">infinite</td>
                    <td class="thead-data">55,000</td>
                    <td class="thead-data">16 Apr 2020, 00:00</td>
                    <td class="thead-data"><span class="pen" @click="showModal1"><font-awesome-icon :icon="['fas', 'pen']"/></span><span class="times"><font-awesome-icon :icon="['fas', 'times']"/></span></td>
                    <td class="thead-data">N/A</td>
                </tr>
                <tr class="next-band">
                    <td class="thead-data">100</td>
                    <td class="thead-data">infinite</td>
                    <td class="thead-data">60,000</td>
                    <td class="thead-data">16 Apr 2020, 00:00</td>
                    <td class="thead-data"><span class="pen" @click="showModal1"><font-awesome-icon :icon="['fas', 'pen']"/></span><span class="times"><font-awesome-icon :icon="['fas', 'times']"/></span></td>
                    <td class="thead-data">N/A</td>
                </tr>
                <tr class="next-band">
                    <td class="thead-data">500</td>
                    <td class="thead-data">infinite</td>
                    <td class="thead-data">100</td>
                    <td class="thead-data">16 Apr 2020, 00:00</td>
                    <td class="thead-data"><span class="pen" @click="showModal1"><font-awesome-icon :icon="['fas', 'pen']"/></span><span class="times"><font-awesome-icon :icon="['fas', 'times']"/></span></td>
                    <td class="thead-data">N/A</td>
                </tr>
                <tr class="next-band">
                    <td class="thead-data">1000</td>
                    <td class="thead-data">100</td>
                    <td class="thead-data">100</td>
                    <td class="thead-data">16 Apr 2020, 00:00</td>
                    <td class="thead-data"><span class="pen" @click="showModal1"><font-awesome-icon :icon="['fas', 'pen']"/></span><span class="times"><font-awesome-icon :icon="['fas', 'times']"/></span></td>
                    <td class="thead-data">N/A</td>
                </tr>
                <tr class="next-band">
                    <td class="thead-data">10,000</td>
                    <td class="thead-data">infinite</td>
                    <td class="thead-data">30,000</td>
                    <td class="thead-data">16 Apr 2020, 00:00</td>
                    <td class="thead-data"><span class="pen" @click="showModal1"><font-awesome-icon :icon="['fas', 'pen']"/></span><span class="times"><font-awesome-icon :icon="['fas', 'times']"/></span></td>
                    <td class="thead-data">N/A</td>
                </tr>
                <tr class="next-band">
                    <td class="thead-data">20,000</td>
                    <td class="thead-data">100,000</td>
                    <td class="thead-data">10,000</td>
                    <td class="thead-data">16 Apr 2020, 00:00</td>
                    <td class="thead-data"><span class="pen" @click="showModal1"><font-awesome-icon :icon="['fas', 'pen']"/></span><span class="times"><font-awesome-icon :icon="['fas', 'times']"/></span></td>
                    <td class="thead-data">10 Feb 2021, 00:00</td>
                </tr>
            </table>
            <div class="smallBoxes">
            <div class="boxes"><font-awesome-icon :icon="['fas', 'chevron-left']"/></div>
            <div class="boxes">1</div>
            <p>...</p>
            <div class="boxes">4</div>
            <div class="boxes">5</div>
            <div class="boxes">6</div>
            <div class="boxes">7</div>
            <div class="boxes">8</div>
            <p>...</p>
            <div class="boxes">50</div>
            <div class="boxes"><font-awesome-icon :icon="['fas', 'chevron-right']"/></div>
            <div>Go to</div>
            <div class="goto" role="input"></div>
            </div>
        </div>
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
        mounted () {
            document.querySelector('#modal-btn').style.display = 'block';
            let Flex = document.querySelector('.flex');
            let name = document.querySelector('.Navname');
            name.textContent = 'Coins';
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
        },
    }
</script>