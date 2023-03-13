<template>
    <div>
        <h2>{{ name }}</h2>
        <p v-html="title" v-bind:class="[class1,class2]" v-bind:id="id1">

        </p>
        <p :class="{success:isActive,popular:isPopular}">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil excepturi quaerat id atque facilis! Consequuntur nobis provident quae, sint vel repellendus animi ex, mollitia maiores atque fugiat possimus fugit impedit?
        </p>
        <button :class="{btnborder:isBorder}">
            {{ btnClick }}
        </button>
        <h3 :class="isPopular && 'popular'">Popular Class</h3>
        <h4 :class="isActive ? class1:'popular'">Active Class</h4>
        <p :class="[isActive ? class1:class2, isBorder && 'btnBorder']">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro iusto eveniet maiores vero aperiam in laborum nesciunt earum fugit, magnam tempora cum aliquid, facere sit, quasi ullam nobis nisi veritatis!
        </p>
        <p :style="{'background-color':'blue','color':'yellow'}">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam, provident nesciunt. Aliquid dicta temporibus neque eos molestiae, nulla eaque veniam assumenda dignissimos nemo. Iure voluptate nihil est autem! Ad, fugiat?</p>
    </div>
</template>
<script>
export default{
    name:'BasicComponent',
    data(){
        return{
            name:'basic component 1',
            title:"<h2>Vue Lessons</h2>",
            class1:'mytitle',
            class2:'textcolor',
            isActive:true,
            isPopular:false,
            id1:'title',
            btnClick:'Click Me',
            isBorder:true,

        }
    }
}
</script>
<style scoped>
.mytitle{
    background-color:red
}
#title{
    text-transform: uppercase;
}
.textcolor{
    color:yellow;
}
.success{
    border:2px solid green;
    padding:5px;
}
.popular{
    text-transform: uppercase;
    color:blue;
}
.btnborder{
    border:2px solid blue;
    border-radius: 5px;
    background-color: yellow;
}
</style>