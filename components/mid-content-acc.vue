<template>
    <div>
        <div class="midDiv">
            <p class="setting">Settings</p> <hr class="hr">
            <h5 class="changePassword">Change Your Password</h5>
            <form>
                <div class="form-group">
                    <label for="currentPassword">Current Password</label>
                    <div class="formInput" role="input">
                        <p>Enter Current Password</p> <span>show</span>
                    </div>
                    <label for="newPassword">New Password</label>
                    <div class="formInput" role="input">
                        <p>Enter New Password</p> <span>show</span>
                    </div>
                    <label for="confirmPassword">Confirm Password</label>
                    <div class="formInput" role="input">
                        <p>Confirm New Password</p> <span>show</span>
                    </div>
                </div>
            </form>
            <div class="btn" role="button">Save changes</div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

</style>