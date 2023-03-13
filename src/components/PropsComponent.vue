<template>
    <div>
        <h2> Page title : {{name}}</h2>
    </div>
</template>

<script>
    export default {
        name:'PropsComponent',
        data(){
            return{

            }
        },
        props:['name']
        
    }
</script>

<style scoped>

</style>