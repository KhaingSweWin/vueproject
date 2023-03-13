<template>
    <div>
        <input type="text" name="" id="" v-model="doctor" class="form-control my-3">
        <select name="" id="" v-model="speciality" class="form-select mb-3">
            <option > Please choose anything</option>
            <option value="heart"> Heart</option>
            <option value="brain"> Brain</option>
            <option value="liver"> LIver</option>
            <option value="heart"> Heart</option>
        </select>
        <button class="btn btn-success">Find Doctor</button>
    </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css'
    export default {
        name:"FindComponent",
        data(){
            return{
                doctor:"",
                speciality:""
            }
        }

    }
</script>

<style scoped>

</style>