<template>
    <div>
        <h2>Child Component</h2>
        <button @click="$emit('hide')">Hide</button>
    </div>
</template>

<script>
    export default {
        name:"ChildComponent",
        data(){
            return{

            }
        },
        emits:['hide']
    }
</script>

<style scoped>

</style>