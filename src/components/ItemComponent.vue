<template>
    <div class="row">
        <div class="col-md-3">
            <p> Name: {{ item.name }} </p>
        </div>
        <div class="col-md-2">
            <p> Price : {{ item.price }} </p>
        </div>
        <div class="col-md-3">
            <input type="number" name="" id="" v-model="qty">
        </div>
        <div class="col-md-2">
            <p>Sub total : {{ qty * item.price }}</p> 
        </div>
        <div class="col-md-2">
            <button @click="addcart(item)" class="btn btn-success">Add to cart</button>
        </div>
    </div>
    <div>     
        
        
        
        
    </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.min.css"
    export default {
        name:'ItemComponent',
        props:['item'],
        emits:['updatecart'],
        methods:{
            addcart(item)
            {
                console.log(`qty is ${this.qty}`)
               return this.$emit('updatecart',item,this.qty)
            }
        },
        data(){
            return{
                qty:0
            }
        }
    }
</script>

<style scoped>

</style>