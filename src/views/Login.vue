<template>
<div class="container">
    <h1>Login to NEU Twitter</h1>
    <br>
    <br>
    <div class="row">
        <div class="col-md-3"></div>
        <div class="col-md-6">
            <form>
                <div class="mb-3">
                    <input type="email" 
                    class="form-control" 
                    id="email"
                    v-model="email"
                    aria-describedby="emailHelp"
                    placeholder="Enter Email">
                </div>
                <div class="mb-3">
                    <input type="password" 
                    class="form-control" 
                    id="password"
                    v-model="password"
                    placeholder="Enter Password">
                    <div v-if="password.length>1 && password.length<6" 
                    class="text-danger">Password lenght should be greater than 6 character</div>
                </div>
                
                <button class="btn btn-primary">Login</button>
            </form>
        </div>
        <div class="col-md-3"></div>
    </div>
</div>
</template>

<script>
export default {
    name: "login",
    data() {
        return {
            email: "",
            password: ""
        }
    },
    methods: {
        login: function() {
            console.log ("Email: " + this.email);
            console.log ("Password: " + this.password);
            
        },
    },

}
</script>

<style lang="scss" scoped>

</style>
