<template>
    <div class="register-form">
        <div class="col-md-12 no-padding">
        <form @submit.prevent="resetPass('reset_pass')" auto-complete="off" data-vv-scope="reset_pass">
            <div class="col-md-12 input-container no-padding">
                    <label for="firstname">Email</label>
                    <div class="input-group">
                        <span class="input-group-addon"><i class="fa fa-envelope"></i></span>
                        <u-input 
                            type="email" 
                            name="email"
                            v-model="reset.email"
                            v-validate="'required|email'"
                            className="form-control custom-input"
                            placeholder="Enter your email address"/> 
                    </div>
                    <small v-show="errors.has('reset_pass.email')" class="form-error animated fadeInUp2">{{ errors.first('reset_pass.email') }}</small>
            </div>
            <br>
            <div class="col-md-12 input-container no-padding">
                <div class="col-md-6 no-padding">
                    <div class="input-group">
                        <u-button 
                            type="submit"
                            class="default-button">Reset Password</u-button>
                    </div>
                </div>
            </div>
        </form>
        </div>
    </div>
</template>
<script>
const inputField = require('./ui/input.vue')
const registerButton = require('./ui/button.vue')
module.exports = {
    data () {
        return {
            reset: {email: ''}
        }
    },
     methods: {
     resetPass (scope) {
        this.$validator.validateAll(scope).then(validate => {

        })
    }
 },
     components: {
     'u-input': inputField,
     'u-button': registerButton

 }
}
</script>
