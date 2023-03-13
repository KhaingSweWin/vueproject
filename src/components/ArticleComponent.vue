<template>
    <div>
        <slot name="title"> 

        </slot>
        <slot name="main"></slot>
        <slot name="footer" :admin="admin"></slot>
    </div>
    
</template>

<script>
    export default {
        name:"ArticleComponent",
        data(){
            return{
                admin:"Host Myanmar",
                
            }
        }
    }
</script>

<style scoped>

</style>