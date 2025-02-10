<!-- <template>
<h2>{{name}}</h2>
<h2>{{user.name}}</h2>
<button v-on:click="getData()">call function</button>

</template>

<script>
export default{
    name:'Child',
    props:{
        name:String,
        user:Object,
        getData:Function
    }
}
</script> -->

<template>
    <div class="child">
        <h2>{{data.name}}</h2>
        <h2>{{data.email}}</h2>
        <button v-on:click="getData(data.name)">Alert Name</button>
    </div>
    
</template>

<script>
export default {
    name:'Child',
    props:{
        data:Object,
        getData:Function
    },
    
}
</script>
<style scoped>
.child{
    background-color: aquamarine;
    padding: 10px;
    border-bottom: 1px solid;
    margin-bottom: 20px;
}
</style>