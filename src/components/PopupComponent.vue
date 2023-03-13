<template>
    <div>
         {{ age }}
         <p>{{ name }}</p>
         <button @click="$emit('close',checkAge())">Check Age</button>
    </div>
</template>

<script>
    export default {
        name:'PopupComponent',
        data(){
            return{
                level:''
            }
        },
        props:['age','name'],
        methods:{
            checkAge()
            {
                
                if(this.age >= 35 )
                {
                    this.level='second level'
                }
                console.log("level is "+this.level)
                return this.level;
            }
         },
        emits:['close'] //step 1
            
            }
</script>

<style scoped>

</style>

