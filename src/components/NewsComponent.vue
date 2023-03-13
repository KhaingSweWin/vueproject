<template>
    <div class="row">
        <div  class="col-md-6" v-for="item in news" :key="item.title">
            <slot name="title" :title="item.title"></slot>
            <slot name="description" :description="item.description"></slot>
        </div>
        
    </div>
</template>

<script>
    export default {
        name:"NewsComponent",
        data(){
            return{
                news:[
                    {title:'News 1',description:'Lorem ipsum dolor sit amet consectetur adipisicing elit'},
                    {title:'News 2',description:'Lorem ipsum dolor sit amet consectetur adipisicing elit'},
                    {title:'News 3',description:'Lorem ipsum dolor sit amet consectetur adipisicing elit'},
                    {title:'News 4',description:'Lorem ipsum dolor sit amet consectetur adipisicing elit'},
                    {title:'News 5',description:'Lorem ipsum dolor sit amet consectetur adipisicing elit'},
                ]
            }
        }
    }
</script>

<style scoped>

</style>