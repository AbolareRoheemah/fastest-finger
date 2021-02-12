<template>
    <div class="modal1">
        
        <div class="modal-body">
                <div class="modal-header">
                    <h1>EDIT COINS <span class="close-btn1" @click="closeModal1">&times;</span></h1>
                </div>
            <div class="label">
                <div>
                    <p>Coin Quantity</p>
                    <input type="text" class="input-box" v-model="Coin_Quantity">
                    <!-- <div  role="input">20,000</div> -->
                </div>
                <div>
                    <p>Price</p>
                    <input type="text" class="input-box" v-model="price">
                    <!-- <div class="input-box" role="input">140,000</div> -->
                </div>
                <div>
                    <p>Quantity</p>
                    <input type="text" class="input-box" v-model="Quantity">
                    <!-- <div class="input-box" role="input">100,000</div> -->
                </div>
                <div>
                    <p>Expiry</p>
                    <div class="input-box" role="select">31 Days&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#"><font-awesome-icon :icon="['fas', 'chevron-down']"/></a></div>
                </div>
            </div>
                <div class="addNewBtn" role="button">Save Changes</div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            Coin_Quantity: '20,000',
            price: "140,000",
            Quantity: "100,000"
        }
    },
    methods: {
        closeModal1() {
            let modalBtn1 = document.querySelector('.pen');
            let modal1 = document.querySelector('.modal1');
            let closeBtn1 = document.querySelector('.close-btn1');
            modal1.style.display = 'none';
        },
    },
}
</script>

<style scoped>
.modal1 {
  display: none;
  position: fixed;
  z-index: 1; 
  padding-top: 10%;
  left: 0; 
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto; 
  background-color: rgb(0, 0, 0);
  background-color: rgba(0, 0, 0, 0.5);
}
.modal-header {
    padding-left: 83px;
    padding-right: 29px;
    padding-top: 26px;
    padding-bottom: 27px;
    background: #F0F2F4;
    display: flex;
    flex-direction: row;
    font-family: 'Overpass';
font-style: normal;
font-weight: 600;
font-size: 16px;
line-height: 25px;
border-radius: 20px 20px 0px 0px;
color: #000000;
}
.modal-body {
  background-color: #FFFFFF;
  margin: auto; 
  width: 70%;  
  animation-name: animatetop;
  animation-duration: 0.4s;
  width: 870px;
    height: 326px;
    border: 1px solid #E2E2EA;
    border-radius: 20px;
}
.close-btn1 {
    cursor: pointer;
  color: #200E32; 
  font-size: 28px;  
  font-weight: bold;
  margin-left: 636px;
mix-blend-mode: normal;
opacity: 0.4; 
}
.close-btn:hover, .close:focus {
  color: darkgray;
  text-decoration: none;
  cursor: pointer;
}
@-webkit-keyframes animatetop {
  from {top:-300px; opacity:0} 
  to {top:0; opacity:1}
}
@keyframes animatetop {
  from {top:-300px; opacity:0}
  to {top:0; opacity:1}
}
.label {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 28px 55px 9px 83px;
    text-align: left;
    font-family: 'Overpass';
font-style: normal;
font-weight: normal;
font-size: 14px;
line-height: 21px;
color: #000000;
}
.input-box {
    width: 165px;
    height: 50px;
    /* text-align: center; */
    border: 1px solid #4B545A;
    box-sizing: border-box;
    border-radius: 3px;
    margin: auto 0;
    padding: 13px 16px;
    color: #818181;
}
.addNewBtn, .addNewBtn:hover {
    cursor: pointer;
    position: absolute;
    width: 234px;
height: 50px;
left: 50%;
transform: translate(-50%, 0);
margin-top: 1.5%;
background: #F1AA83;
box-shadow: 0px 3px 0px #EA9975;
border-radius: 20px;
text-align: center;
align-items: center;
text-transform: uppercase;
padding-top: 16px;
font-family: 'Rubik';
font-style: normal;
font-weight: bold;
font-size: 14px;
line-height: 17px;

color: #B67C62;
}
</style>