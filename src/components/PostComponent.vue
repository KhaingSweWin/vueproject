<template>
    
    <div >
        <slot :greet="name">
           
        </slot>
        <slot name="title"></slot>
        <slot name="content" v-bind="$attrs">
           
        </slot>
        <slot name="footer"></slot>
    </div>
</template>

<script>
    export default {
        name:"PostComponent",
        data(){
            return{
                name:"khaing"
            }
        }
    }
</script>

<style scoped>
#mydiv{
    background-color:red
}
</style>