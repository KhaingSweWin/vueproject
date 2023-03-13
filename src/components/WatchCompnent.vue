<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <input type="text" name="" id="" class="form-control" v-model="nickname">
                    <input type="text" name="" id="" class="form-control" v-model="surname">
                   
                </div>
                <div class="col-md-6">
                    <p> {{  fullname }}</p>
                    <p> Computed Name : {{  full_name }}</p>
                </div>
            </div>
            <div class="row">
                <div class="col-md-6">
                    <input type="number" name="" id="" v-model="fah" class="form-control">
                    <p>=</p>
                    <input type="number" name="" id="" v-model="cel" class="form-control">
                </div>
            </div>
            <div class="row">
                <div class="col-md-6">
                    <input type="text" name="" id="" v-model="student.name" class="form-control">
                    <input type="text" name="" id="" v-model="student.age" class="form-control">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css'
    export default {
       name:'WatchComponent',
       data(){
        return{
            nickname:"Shelly",
            surname:"Bluion",
            fullname:'',
            fah:50,
            cel:0,
            student:{
                name:'',
                age:''
            }
        }
       }, 
       watch:{
           nickname(newname,oldname)
           {
            console.log(oldname)
             this.fullname= newname +" "+ this.surname
           },
           surname(newname){
            console.log(newname)
            this.fullname=this.nickname+ " "+newname
           },
           fah:{
            handler(newF,oldF){
                console.log("new fah "+newF)
             if(newF==120 && newF> oldF)
             {
                alert("it is over 120");
             }
             this.cel=(newF-32)*5/9;
            },
            immediate:true
           },
           cel(newC){
            this.fah=(newC*(9/5))+32
           },
           student:{
            handler(newValue)
            {
                console.log(newValue.name + "==="+newValue.age)
            },
            deep:true
            
        }


       },
       computed:{
        full_name(){
           return this.nickname + " "+this.surname
        }
       }
    }
</script>

<style scoped>

</style>