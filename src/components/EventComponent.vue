<template>
    <div>
        <button @click="index++">Increase</button> 
        <span>{{ index }}</span>
    </div>
    <div>
        <button @click="decrease($event)">decrease</button>
        <span> {{  index }}</span>
    </div>
    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <form action="" @submit="register($event)">
                    <div>
                        <label for="" class="form-label"> Name </label>
                        <input type="text" name="" id="" class="form-control" v-model="form.name">
                    </div>
                    <div>
                        <label for="" class="form-label"> Email </label>
                        <input type="email" name="" id="" class="form-control" v-model="form.email">
                    </div>
                    <div>
                        <label for="" class="form-label"> Address</label>
                        <input type="text" name="" id="" class="form-control" v-model="form.address">
                    </div>
                    <div class="mt-4">
                        <input type="radio" name="" id="" class="form-check-input" value="male" v-model="form.gender">
                         <label for="" class="form-check-label">Male</label>
                         <input type="radio" name="" id="" class="form-check-input" value="female" v-model="form.gender">
                         <label for="" class="form-check-label">Female</label>
                    </div>
                    <div class="mt-4">
                        <select name="" id="" class="form-select" v-model="form.course">
                            <option value="">Select a course</option>
                            <option value="php">PHP</option>
                            <option value="java">Java</option>
                            <option value="react">REact</option>
                        </select>
                        
                    </div>
                    <div class="mt-4">
                        <button type="submit" class="btn btn-success" >Register</button>
                    </div>
                </form>
            </div>
            <div class="col-md-6">
                {{ JSON.stringify(form) }}
            </div>
            <div class="col-md-6">
                <ul v-for="student in students" :key="student.name">
                    <li>{{ student.name }}, {{  student.email }}, {{ student.address }}</li>
                </ul>
            </div>
        </div>
    </div>
    
</template>
<script>
import 'bootstrap/dist/css/bootstrap.min.css'
export default{
    name:'EventComponent',
    data(){
        return{
           index:0,
           form :{
            name:'',
            email:'',
            address:'',
            gender:'',
            course:''
           },
           students:[]
        }
    },
    methods:{
        decrease(event){
            event.preventDefault();
            if(event)
            {
                console.log(event)
                event.preventDefault();
                this.index--;
            }

        },
        register(event){
            event.preventDefault();
            console.log(this.form.name)
            this.students.push({
                name: this.form.name,
                email:this.form.email,
                address:this.form.address
            });
        }
    }
}
</script>

<style scoped>

</style>