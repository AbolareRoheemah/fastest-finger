<template>
    <div>
        <table class="paddi">
                <tr class="next-band" v-for="info in infos" :key="info.Price">
                    <td class="thead-data">{{ info.Coin_Quantity }}</td>
                    <td class="thead-data">{{ info.Quantity }}</td>
                    <td class="thead-data">{{ info.Price }}</td>
                    <td class="thead-data">{{ info.Date_Created }}</td>
                    <td class="thead-data"><span class="pen" @click="showModal1"><font-awesome-icon :icon="['fas', 'pen']"/></span><span class="times" @click="deleteCoin"><font-awesome-icon :icon="['fas', 'times']"/></span></td>
                    <td class="thead-data">{{ info.Expiry }}</td>
                </tr>
        </table>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                infos: [
                    {
                       Coin_Quantity: 100,
                        Quantity: 'infinte',
                        Price: '55,000',
                        Date_Created: '16 Apr 2020, 00:00',
                        Action: 'action',
                        Expiry: 'N/A' 
                    },
                    {
                       Coin_Quantity: 100,
                        Quantity: 'infinte',
                        Price: '55,000',
                        Date_Created: '16 Apr 2020, 00:00',
                        Action: 'action',
                        Expiry: 'N/A' 
                    },
                    {
                       Coin_Quantity: 100,
                        Quantity: 'infinte',
                        Price: '55,000',
                        Date_Created: '16 Apr 2020, 00:00',
                        Action: 'action',
                        Expiry: 'N/A' 
                    },
                    {
                       Coin_Quantity: 100,
                        Quantity: 'infinte',
                        Price: '55,000',
                        Date_Created: '16 Apr 2020, 00:00',
                        Action: 'action',
                        Expiry: 'N/A' 
                    },
                    // {
                    //    Coin_Quantity: 100,
                    //     Quantity: 'infinte',
                    //     Price: '55,000',
                    //     Date_Created: '16 Apr 2020, 00:00',
                    //     Action: 'action',
                    //     Expiry: 'N/A' 
                    // },
                    // {
                    //    Coin_Quantity: 100,
                    //     Quantity: 'infinte',
                    //     Price: '55,000',
                    //     Date_Created: '16 Apr 2020, 00:00',
                    //     Action: 'action',
                    //     Expiry: 'N/A' 
                    // },
                ],
            }
        },
        methods: {  
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
    }
</script>

<style lang="scss" scoped>

</style>