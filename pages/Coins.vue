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
            <!-- <NuxtChild /> -->
            <tbody>
                <tr class="next-band" v-for="p in displayedPosts" :key="p">
            <td class="thead-data">{{ p.Coin_Quantity }}</td>
            <td class="thead-data">{{ p.Quantity }}</td>
            <td class="thead-data">{{ p.Price }}</td>
            <td class="thead-data">{{ p.Date_Created }}</td>
            <td class="thead-data"><span class="pen" @click="showModal1"><font-awesome-icon :icon="['fas', 'pen']"/></span><span class="times" @click="deleteCoin"><font-awesome-icon :icon="['fas', 'times']"/></span></td>
            <td class="thead-data">{{ p.Expiry }}</td>
        </tr>
            </tbody>
            </table>
            <ul class="smallBoxes">
                <li v-if="page != 1">
                    <button class="boxes" @click="page--"><font-awesome-icon :icon="['fas', 'chevron-left']"/></button>
                </li>
                <li>
                    <button class="boxes" type="button" v-for="pageNumber in pages.slice(page-1, page+5)" :key="pageNumber" @click="page = pageNumber">{{ pageNumber }}</button>
                </li>
                <li v-if="page < pages.length">
                    <button type="button" class="boxes" @click="page++"><font-awesome-icon :icon="['fas', 'chevron-right']"/></button>
                </li>
            </ul>
        </div>
        <div class="marginTest"></div>
    </div>
</template>

<script>
import AddModal from '~/components/new-coins-modal.vue';
import EditCoin from '~/components/editCoins.vue';
    export default {
        data() {
            return {
                posts: [],
                page: 1,
                perPage: 7,
                pages: [1, 2, 3]
            }
        },
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
            getPosts() {
                let data = [];
                for (let i =0; i < 7; i++) {
                    this.posts.push({
                       Coin_Quantity: 100,
                        Quantity: 'infinte',
                        Price: '55,000',
                        Date_Created: '16 Apr 2020, 00:00',
                        Action: 'action',
                        Expiry: 'N/A' 
                    });
                }
                for (let i = 0; i < 7; i++) {
                    this.posts.push({
                       Coin_Quantity: 500,
                        Quantity: 'infinte',
                        Price: '95,000',
                        Date_Created: '21 Apr 2021, 20:08',
                        Action: 'action',
                        Expiry: 'A/c' 
                    });
                }
                for (let i = 0; i < 7; i++) {
                    this.posts.push({
                       Coin_Quantity: 900,
                        Quantity: 'infinte',
                        Price: '50,000',
                        Date_Created: '20 Jun 2021, 20:08',
                        Action: 'action',
                        Expiry: 'A/C' 
                    });
                }
            },
            // setPages() {
            //     let numberOfPages = Math.ceil(this.posts.length / this.perPage);
            //     for (let index = 1; index <= (numberOfPages); index++) {
            //         this.pages.push(index);
            //     }
            // },
            paginate(posts) {
                let page = this.page;
                let perPage = this.perPage;
                let from = (page * perPage) - perPage;
                let to = (page * perPage);
                return posts.slice(from, to);
            }
        },
        computed: {
            displayedPosts() {
                return this.paginate(this.posts); 
            }
        },
        // watch: {
        //     posts() {
        //         this.setPages();
        //     }
        // },
        created () {
            this.getPosts();
        },
        filters: {
            trimWords(value){
            return value.split(" ").splice(0,20).join(" ") + '...';
            }
        }
    }
</script>