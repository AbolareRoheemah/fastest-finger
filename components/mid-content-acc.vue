<template>
    <div>
        <div class="midDiv">
            <p class="setting">Settings</p> <hr class="hr">
            <h5 class="changePassword">Change Your Password</h5>
            <form>
                <div class="form-group">
                    
                    <label for="currentPassword">Current Password</label>
                    <div class="contain">
                        <input class="formInput" id="password1" type="password" placeholder="Enter Current Password"/>
                        <span class="showToggler" id="showToggler1" @click="togglePass1">show</span>
                    </div>
                        
                    <label for="newPassword">New Password</label>
                    <div class="contain">
                        <input class="formInput" id="password2" type="password" placeholder="Enter New Password"/>
                        <span class="showToggler" id="showToggler2" @click="togglePass2">show</span>
                    </div>
                    
                    <label for="confirmPassword">Confirm Password</label>
                    <div class="contain">
                        <input class="formInput" id="password3" type="password" placeholder="Confirm New Password"/>
                        <span class="showToggler" id="showToggler3" @click="togglePass3">show</span>
                    </div>
                </div>
            </form>
            <div class="btn" role="button">Save changes</div>
        </div>
    </div>
</template>

<script>
    export default {
        methods: {
            togglePass1() {
                let showBtn1 = document.querySelector('#showToggler1');
                let passwordInput1 = document.querySelector('#password1');
                if (passwordInput1.type === 'password') {
                    passwordInput1.type = 'text'
                    showBtn1.textContent = 'hide';
                    if (passwordInput1.value != '') {
                        showBtn1.textContent = 'hide';
                    } else {
                        showBtn1.textContent = 'show';
                    }
                } else {
                    passwordInput1.type = 'password';
                    showBtn1.textContent = 'show';
                }
            },
            togglePass2() {
                let showBtn2 = document.querySelector('#showToggler2');
                let passwordInput2 = document.querySelector('#password2');
                if (passwordInput2.type === 'password') {
                    passwordInput2.type = 'text'
                    showBtn2.textContent = 'hide';
                    if (passwordInput2.value != '') {
                        showBtn2.textContent = 'hide';
                    } else {
                        showBtn2.textContent = 'show';
                    }
                } else {
                    passwordInput2.type = 'password';
                    showBtn2.textContent = 'show';
                }
            },
            togglePass3() {
                let showBtn3 = document.querySelector('#showToggler3');
                let passwordInput3 = document.querySelector('#password3');
                if (passwordInput3.type === 'password') {
                    passwordInput3.type = 'text'
                    if (passwordInput3.value != '') {
                        showBtn3.textContent = 'hide';
                    } else {
                        showBtn3.textContent = 'show';
                    }
                } else {
                    passwordInput3.type = 'password';
                    showBtn3.textContent = 'show';
                }
            }
        },
    }
</script>

<style scoped>
.contain {
    position: relative;
    /* padding: auto; */
    width: 50%;
    left: 50%;
    transform: translate(-50%, 0);
    
}
.showToggler, .showToggler:hover {
    position: absolute;
    left: 18vw;
    top: 50%;
    transform: translate(0, -50%);
    font-family: 'Overpass';
    font-size: 12px;
    line-height: 18px;
    text-align: right;
    color: #818181;
    font-size: 1.1em;
    cursor: pointer;
}
</style>