<template>
    <div>
        <input type="text" v-model="marks">
        <p v-if="marks <75 "> Grade B</p>
        <p v-else>Grade A</p>
        <div>
            <p v-if="(number%2)==0" :class="even"> Even</p>
            <p v-else :class="odd">Odd</p>
        </div>
        <div>
            <p v-show="show"> Show Element</p>
        </div>
    </div>
</template>
<script>
export default{
    name:'ConditionComponent',
    data(){
        return{
            marks:75,
            number : 14,
            even:'even',
            odd:'odd',
            show:false
        }
    }

}
</script>
<style scoped>

</style>