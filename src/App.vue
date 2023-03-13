<template>
  <div class="container">
       <div class="row">
          <div class="col-md-6">
            <button @click="activeSearch='SearchComponentVue'"> Search by Organ</button>
            <button @click="activeSearch='FindComponentVue'"> Find Doctor</button>
            <component :is="activeSearch">

            </component>

          </div>
       </div>
    </div>
  <!-- <EventComponent></EventComponent> -->
    <!-- <ListComponentVue></ListComponentVue> -->
    <!-- <ToDoComponent></ToDoComponent> -->
    <!-- <PropsComponent :name="header"></PropsComponent>
    <PropsComponent name="sidenav"></PropsComponent>
    <PropsComponent name="footer"></PropsComponent>
    <WatchComponent></WatchComponent> -->
    <!-- <div class="container">
      <div class="row">
        <div class="col-md-6">
          <input type="text" name="" id="" v-model="name" class="form-control mb-4" >
          <input type="number" name="" id="" v-model="age" class="form-control">
        </div>
        <div class="col-md-6">
          <PopupComponent :age='age' :name="name" @close="getLevel"></PopupComponent>
          {{ message }}
        </div>
      </div>
      <div class="row mt-5">
        <div class="col-md-6">
          <button class="btn btn-primary" @click="show">Show Component</button>
        </div>
        <div class="col-md-6">
          <ChildComponent v-show="showUp" @hide="showUp=false"></ChildComponent>
        </div>
      </div>
    </div>   -->
    <!-- <ItemComponent v-for="item in itemList" :key="item.name" :item="item" @updatecart="update">

    </ItemComponent>
    <p>Number of items in this cart : {{ total }}</p>
    <p>Total cost is {{ totalcost }}</p> -->
    <!-- <div class="container">
      <div class="row">
        <div class="col-md-4">
          <PostComponent class="mypost">
              <template v-slot:default="slotpro">
                   <h2> {{ slotpro.greet }}</h2>

              </template>
              <template v-slot:title>
                  <h2>Post Title</h2>
              </template>
              <template v-slot:content> 
                <img src="./assets/logo.png" alt="hello">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Architecto ipsam sint non necessitatibus tenetur praesentium laborum consectetur. Atque odio possimus earum fuga ea quisquam, inventore nisi asperiores sunt magnam iste!
                </p>
              </template>
              <template v-slot:footer>
                <button class="btn btn-primary"> See More</button>
              </template>
          </PostComponent>
        </div>
        <div class="col-md-4">
          <PostComponent>
              <template v-slot:title>
                  <h2>Post Title</h2>
              </template>
              <template v-slot:content> 
                <img src="./assets/logo.png" alt="hello">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Architecto ipsam sint non necessitatibus tenetur praesentium laborum consectetur. Atque odio possimus earum fuga ea quisquam, inventore nisi asperiores sunt magnam iste!
                </p>
              </template>
              <template v-slot:footer>
                <button class="btn btn-primary"> See More</button>
              </template>
          </PostComponent>
        </div>
        <div class="col-md-4">
          <PostComponent>
              <template v-slot:title>
                  <h2>Post Title</h2>
              </template>
              <template v-slot:content> 
                <img src="./assets/logo.png" alt="hello">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Architecto ipsam sint non necessitatibus tenetur praesentium laborum consectetur. Atque odio possimus earum fuga ea quisquam, inventore nisi asperiores sunt magnam iste!
                </p>
              </template>
              <template v-slot:footer>
                <button class="btn btn-primary"> See More</button>
              </template>
          </PostComponent>
        </div>
      </div>
      <div class="row">
          <div class="col-md-4" v-for="post in posts" :key="post.title">
            <PostComponent>
              <template v-slot:titel>
                  <h2> {{ post.title }}</h2>
              </template>
              <template v-slot:content>
                <img :src="post.imgsrc" alt="hello">
                  <p> {{  post.content }}</p>
                  
              </template>
              <template v-slot:footer>
                <div>
                  <button class="btn btn-success"> See More</button>
                </div>
                  
              </template>
            </PostComponent>
          </div>
      </div>

    </div>
   
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <button @click="activeTab='Tab1Component'">Tab 1</button>
          <button @click="activeTab='Tab2Component'">Tab 2</button>
          <button @click="activeTab='Tab3Component'">Tab 3</button>
        </div>
        <div class="col-md-6">
          <keep-alive>
            <component :is="activeTab" @display="showname">

            </component>
          </keep-alive>
         
           <Tab1ComponentVue v-if="activeTab=='Tab1Component'"></Tab1ComponentVue>
          <Tab2ComponentVue v-if="activeTab=='Tab2Component'"></Tab2ComponentVue>
          <Tab3ComponentVue v-if="activeTab=='Tab3Component'"></Tab3ComponentVue> -->
        <!-- </div>
      </div>
    </div> --> 
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <ArticleComponent>
            <template v-slot:title>
                  <h2> Covid 19 in 2020</h2>
            </template>
            <template v-slot:main>
                  <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi illum consequatur, est eos voluptatibus voluptas minima, maxime obcaecati nihil hic vero, harum eligendi esse omnis ea earum dolore quidem quas.</p>
                  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim vero porro eos est dolorum aut qui sunt dicta facilis vel unde officia, dignissimos, incidunt ducimus impedit? Distinctio quo eveniet suscipit?</p>
                  <img src="./assets/flower.jpg" alt="" class="article_image">
            </template>
         </ArticleComponent>
        </div>
        <div class="col-md-6">
          <ArticleComponent>
              <template v-slot:title>
                    <h2> Vue Lessons (HMM)</h2>
              </template>
              <template v-slot:main>
                 <ul>
                  <li v-for="lesson in lessons" :key="lesson">
                    {{  lesson }}
                  </li>
                 </ul>
              </template>
              <template v-slot:footer="slotProp">
                  <hr>
                  <div>
                    Posted By {{ slotProp.admin }}
                  </div>
              </template>
            
          </ArticleComponent>
        </div>
      </div>
    </div>
    <div class="container">
        
          
            <NewsComponent>
              <template v-slot:title="newsProps">
                  <h2> {{ newsProps.title }}</h2>
              </template>
              <template v-slot:description="descProps">
                  <p> {{  descProps.description }}</p>
              </template>
            </NewsComponent>
            
         
        
    </div>
    
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css';
import ArticleComponent from './components/ArticleComponent.vue';
import NewsComponent from './components/NewsComponent.vue';

import SearchComponentVue from './components/SearchComponent.vue';
import FindComponentVue from './components/FindComponent.vue';
// import PostComponent from './components/PostComponent.vue';

// import Tab1Component from './components/Tab1Component.vue';
// import Tab2Component from './components/Tab2Component.vue';
// import Tab3Component from './components/Tab3Component.vue';

// import ItemComponent from './components/ItemComponent.vue';
// import BasicComponentVue from './components/BasicComponent.vue' //step 1 component registraiton
// import ConditionComponent from './components/ConditionComponent.vue';
// import ListComponentVue from './components/ListComponent.vue';
//import EventComponent from './components/EventComponent.vue';
//import ToDoComponent from './components/ToDoComponent.vue';
// import WatchComponent from './components/WatchCompnent.vue';
// import PropsComponent from './components/PropsComponent.vue';
// import PopupComponent from './components/PopupComponent.vue';
// import ChildComponent from './components/ChildComponent.vue';

export default {
  name: 'App',
  components:{
  // ListComponentVue//step 2
  //EventComponent
   // ToDoComponent
  //  WatchComponent,PropsComponent
  //PopupComponent,ChildComponent
  //ItemComponent
  // PostComponent,
  // Tab1Component,Tab2Component,Tab3Component
  ArticleComponent,NewsComponent,SearchComponentVue,FindComponentVue
  },
  data(){
    return{
      header:"Host Myanmar Web Site",
      age:0,
      name:'',
      message:'',
      showUp:false,
      itemList:[
        {name:'Laptop',price:450,qty:0, discount:0.02},
        {name:'Phone',price:200,qty:0},
        {name:'Adapter',price:45,qty:0}
      ],
      cart:[],
      total:0 ,
      totalcost:0  ,
      posts:[
        {title:"Post 1", content:"posts 1 content",imgsrc:require("./assets/logo.png")},
        {title:"Post 2", content:"posts 2 content",imgsrc:require("./assets/logo.png")},
        {title:"Post 3", content:"posts 3 content",imgsrc:require("./assets/logo.png")},
        {title:"Post 1", content:"posts 1 content",imgsrc:require("./assets/logo.png")},
        {title:"Post 2", content:"posts 2 content",imgsrc:require("./assets/logo.png")},
        {title:"Post 3", content:"posts 3 content",imgsrc:require("./assets/logo.png")}
      ]  ,
      activeTab:"Tab1Component" ,
      lessons:['Vue Lessons','v-bind class','Props','Emitted Custome Events'] ,
      activeSearch:"SearchComponentVue"
      
    }
  },
  methods:{
    getLevel(message)
    {
      console.log(message)
      this.message=message;
    },
    show()
    {
      this.showUp=true;
    },
    update(product,qty)
    {
      this.totalcost=0;
      product.qty=qty;
      this.cart.push(product)
      console.log(this.cart)
      console.log(qty)
      this.cart.forEach(element => {
        this.totalcost+=element.price * element.qty
      });
      this.total+=product.qty;
    },
    showname(name){
      console.log("anme is "+name)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  color: #2c3e50;
  margin-top: 60px;
}
#post{
  width:400px;
  height:500px;
  border:2px solid black;
  background-color:blue;
}
.article_image{
  width:100%;
  height:400px;
}
</style>
