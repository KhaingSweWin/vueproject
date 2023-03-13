<template>
    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <div>
                    <input type="text" name="newtask"  id="" class="form-control" v-model="newtask">
                    <button class="btn btn-primary mt-3" @click="addtask"> Add</button>
                    <input type="text"  :value="data" @input="add($event)" class="form-control">
                    {{ data }}
                </div>
            </div>
            <div class="col-md-6">
                <ul v-for="task in tasklist" :key="task.id">
                    <li> 
                        <div class="row">
                            <div class="col-md-6">
                                {{ task.task }} 
                            </div>
                            <div class="col-md-6">
                                <button class="btn btn-danger" @click="removeTask(task)">X</button>
                            </div>
                        </div>
                        
                       
                    </li>
                </ul>
                <p>Method Name {{ callName() }}</p>
                <p>Computed Name {{ naming }}</p>
                <p>Full Name {{ fullName }}</p>
                <button @click="changeName">Change name</button>
            </div>
        </div>
    </div>
</template>
<script>
import 'bootstrap/dist/css/bootstrap.min.css'
export default{
    name:'ToDoComponent',
    data(){
        return{
            id:0,
            newtask:'',
            tasklist:[],
            data:'',
            nickname:'Willy',
            surnmae:'Bluoin'
            
        }
    },
    methods:{
        addtask(){
            this.tasklist.push({id:this.id++, task:this.newtask})
            //this.tasklist.push(this.newtask)
            this.newtask="";
        },
        add(event)
        {
            this.data=event.target.value
        },
        removeTask(task)
        {
            console.log("remove task"+task.id)
            this.tasklist= this.tasklist.filter((t) => t!=task )
        },
        callName()
        {
            console.log("methods "+this.nickname)
            return `${this.nickname},${this.surnmae}`
        },
        changeName(){
            this.nickname="Host Myanmar"
            this.fullName="Host Myanmar"
        }
    },
    computed:{
        naming(){
            console.log("computed "+this.nickname)
            return `${this.nickname}:${this.surnmae}`
        },
        fullName:{
            get()
            {
                return `${this.nickname}:${this.surnmae}`
            },
            set(value)
            {
                let names=value.split(' ');
                this.nickname=names[0]
                this.surnmae=names[1]
            }
        }
    }
}
</script>
<style scoped>

</style>