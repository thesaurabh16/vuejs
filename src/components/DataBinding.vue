<template>
    <input type="text" placeholder="enter email" v-model="email"/>
        <br/>
        <br/>
        <input type="password" placeholder="enter Password" v-model="password"/>
        <br/>
        <br/>
        <button v-on:click="getData()" type="button">Get values</button>

    <h3 v-bind:class="{active: isActive}">hey,how you doing</h3>
    <h1>{{ text }}</h1>
    <div v-html="tag"></div>
    <div v-html="tag2"></div>
    <h1>class binding</h1>
    <h2  :class="applystyle">Components</h2>
    <button v-on:click="colorful=!colorful">style</button>
    </template>
    
    <script>
    export default{
        name: 'DataBinding',
        
        data(){
            return{
                email:null,
                password:null,
                isActive:true,
                text:"Gautam",
                tag:'<h1>Bibek</h1>',
                tag2:'<h1>Bibek@gmail.com</h1>',
                colorful:true
            }
        },
        methods:{
            getData(){
                console.warn("Values: ", this.email,this.password)
            }
        },
        computed:{
            applystyle(){
                return{
                    green:this.colorful,
                    error:true,
                    other:false
                }
            }
        }
    }
    </script>
<style scoped>
    .active{
        color: aquamarine;
    }
    .green{
        background-color: green;
        width: 300px;
        padding: 10px;
    }
    .error{
        color: red;

    }
    .other{
        font-size: 50px;
    }
</style>