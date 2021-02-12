<template>
    <div class="modal">
        
        <div class="modal-body">
                <div class="modal-header">
                    <h1>NEW COINS <span class="close-btn" @click="closeModal">&times;</span></h1>
                </div>
            <div class="label">
                <div>
                    <p>Coin Quantity</p>
                    <input type="text" class="input-box" v-model="Coin_Quantity">
                    <!-- <div class="input-box" role="input">Enter Quantity</div> -->
                </div>
                <div>
                    <p>Price</p>
                    <input type="text" class="input-box" v-model="price">
                    <!-- <div class="input-box" role="input">Please Enter</div> -->
                </div>
                <div>
                    <p>Quantity</p>
                    <input type="text" class="input-box" v-model="Quantity">
                    <!-- <div class="input-box" role="input">Please Enter</div> -->
                </div>
                <div>
                    <p>Expiry</p>
                    <div class="input-box" role="select">Please Select&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#"><font-awesome-icon :icon="['fas', 'chevron-down']"/></a></div>
                </div>
            </div>
                <div class="addNewBtn" role="button">Add New Coins</div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            Coin_Quantity: 'Enter Quantity',
            price: "Please Enter",
            Quantity: "Please Enter"
        }
    },
    methods: {
        closeModal() {
            let modalBtn = document.querySelector('#modal-btn');
            let modal = document.querySelector('.modal');
            let closeBtn = document.querySelector('.close-btn');
            modal.style.display = 'none';
        }
    },
}
</script>


<style scoped>
.modal {
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
  /* position: relative;  */
  background-color: #FFFFFF;
  /* padding: 20px;  */
  margin: auto; 
  width: 70%;  
  /* -webkit-animation-name: animatetop;
  -webkit-animation-duration: 0.4s; */
  animation-name: animatetop;
  animation-duration: 0.4s;
  width: 870px;
    height: 326px;
    border: 1px solid #E2E2EA;
    border-radius: 20px;
}
.close-btn {
  /* float: right;  */
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