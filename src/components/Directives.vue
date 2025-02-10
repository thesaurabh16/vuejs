<!-- <template>
    <h1 v-if="show">if  condition</h1>
    <h1 v-else>else condition</h1>
    <button v-on:click="show=false">click</button> 
     <button v-on:click="show=!show">click</button>
</template>
<script>
export default{
    name:'Directives',
    data(){
        return{
            show:true
        }
    }
}
</script> -->

<!-- <template>
    <h1>for condition</h1>
    <ul>
        <li v-for="item in technology" :key="item">
            {{ item }}
        </li>
    </ul>
    <br/>
    <br/>
    <ul>
        <li v-for="item in users" :key="item.email">
            {{ item.name }}
            {{ item.email }}
        </li>
    </ul>
</template>
<script>
export default{
    name:'Directives',
    data(){
        return{
            technology:['java','php','vue','react'],
            users:[
                {name:"saurabh",email:"saurabh@gmail.com"},
                {name:"gopal",email:"gopal@gmail.com"},
                {name:"hari",email:"hari@gmail.com"},
            ]
        }
    }
}
</script> -->

<template>
    <h1 v-if="show">if  condition</h1>
    <h1 v-show="show">show condition</h1>
</template>
<script>
export default{
    name:'Directives',
    data(){
        return{
            show:false
        }
    }
}
</script>