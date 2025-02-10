<!-- <template>
    <h1 v-bind:class=h1>Pass data to child components</h1>
    <Child name="saurabh" :user="user" :getData="getData"/>
</template>

<script>
import Child from './Child.vue';
export default {
    name:"Parent",
    components:{
        Child
    },
    data(){
        return{
            user:{name:'bibek',email:'bibek@gmail.com'}
        }
    },
    methods:{
        getData(){
            console.warn("Parent Function called")
            alert("parent")
        }
    }
}
</script>
<style scoped>
h1{
    color: orange;
}
</style> -->
<template>
    <h1 v-bind:class=h1>Reusable components</h1>
    <ul>
        <li v-for="item in childs" :key="item.name">
            <Child :data="item" :getData="getData"/>
            <!-- {{item.name}}
            {{ item.email }} -->
        </li>
    </ul>
    
</template>

<script>
import Child from './Child.vue';
export default {
    name:"Parent",
    components:{
        Child
    },
    methods:{
        getData(name){
            alert(name)
        }
    },
    data(){
        return {
            childs:[
                {name:'anil',email:'anil@gmail.com'},
                {name:'bibek',email:'bibek@gmail.com'},
                {name:'aviraj',email:'aviraj@gmail.com'},
                {name:'bikin',email:'bikin@gmail.com'},
            ]
        }
    }
    
}
</script>
<style scoped>
h1{
    color: orange;
}
</style>