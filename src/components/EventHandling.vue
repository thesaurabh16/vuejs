<template>
<br>
<br>
<h1 v-on:mousemove="getConsole()">Event Handling</h1>
<button v-on:click="getData('Button 1 clicked')">Click me </button>
<button v-on:dblclick="getData('Button double clicked')">Click me </button>
<br>
<br>
<button @click="getDatas('Button 1 clicked')">Click me </button>
<button @click="increment(1,$event)">Click me </button>
<button @click="decrement(1)">Click me </button>
<h2>{{ count }}</h2>
<h1>{{ name }}</h1>
<button v-on:click="changeName($event), increment(1, $event)">change name</button>
</template>

<script>
export default{
    name:'EventHandling',
    data(){
        return {
            name:'saurabh',
            count:0
        }
    },
    methods:{
        getData(data){
            alert(data);
        },
        getDatas(){
            this.count= this.count+1;
        },
        getConsole(){
            console.warn('function called')
        },
        increment(num, event){
            this.count +=num
            console.log('Event',event)
        },
        decrement(num){
            this.count -=num
        },
        changeName(event){
            this.name = 'Batman',
            console.log('Event',event)
        }
    }
}
</script>