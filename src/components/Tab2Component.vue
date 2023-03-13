<template>
    <div>
        <input type="text" name="" id="" v-model="name" @input="getname">
    </div>
</template>

<script>
    export default {
        name:"Tab2Component",
        data(){
            return{
                name:""
            }
        },
        methods:{
            getname()
            {
                return this.$emit('display',this.name)
            }
        },
        emits:['display']
    }
</script>

<style scoped>

</style>