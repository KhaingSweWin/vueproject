<template>
    <div>
        <div>
            <input type="text" name="" id="" v-model="name">
            <button v-on:click="add">Add name</button>
            <button v-on:click="remove">Remove name</button>
        </div>
        <div>
            <input type="text" v-model.number="num1">
            <input type="text" v-model.number="num2">
            <input type="text" v-model="result">
            <button v-on:click="addition">Add</button>
        </div>
        <p v-for="(student,index) in students" :key="student"> {{ index }} {{  student }} </p>
        <table :class="mytable">
            <tr v-for="(engineer,index) in engineers" :key="engineer.name">
                <td>{{ index+1 }}</td>
                <td> {{ engineer.name }}</td>
                <td>{{ engineer.age }}</td>
                 <td>{{ engineer.address }}</td>
            </tr>
        </table>
        <div>
            <ul v-for="(n,index) in 10" :key="n">
                    <li>{{ index }} => {{ n }} </li>
                    <li v-if="n%2==0"> {{ n  }} is Even</li>
                    <li v-else>{{ n }} is Odd</li>
            </ul>
        </div>
        
    </div>
</template>
<script>
export default{
    name:'ListComponent',
    data(){
        return{
            name:"HMM",
            num1:0,
            num2:0,
            result:0,
            mytable:"mytable",
            students:['Thiri','Hnin Hnin',"Zaw Zaw"],
            engineers:[
                {
                    name:"David",
                    age:30,
                    address:"US"
                },
                {
                    name:"Bruce",
                    age:26,
                    address:"Hong Kong"
                },
                {
                    name:"David",
                    age:30,
                    address:"US"
                },
                {
                    name:"Bruce",
                    age:26,
                    address:"Hong Kong"
                }
            ]
        }
    },
    methods:{
        add(){
            console.log(this.name)
            this.students.push(this.name)
            this.name="";
        },
        remove(){
            this.students.pop();
        },
        addition(){
            this.result=this.num1+this.num2
        }
    }
}
</script>
<style scoped>
    .mytable{
       display:flex;
       align-items: center;
    }
</style>