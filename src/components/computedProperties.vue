<template>
<h2>FullName - {{ firstName }} {{ lastName }}</h2>
<h2>Computed FullName-{{ fullName }}</h2>
<button @click="changeFullName">change fullname</button>
<h2>Totals - {{ items.reduce((total,curr)=>(total = total + curr.price), 0) }}</h2>
<button @click="items.push({id:4,title:'keyboard',price:100})">Add Item</button>
<h2>Computed Total - {{ total }}</h2>
<h2>Method Total - {{ getTotal() }}</h2>
<input type="text" v-model="country">

<template v-for="item in items" :key="item.id">
<h2 v-if="item.price>400">{{ item.title }} {{ item.price }}</h2>
</template>
<h2 v-for="item in expensiveItems" :key="item.id">{{ item.title }} {{ item.price }}</h2>
</template>

<script>


export default{
    name:'computedProperties',
    data(){
        return{
            firstName:'saurabh',
            lastName:'shah',
            items:[
                {
                    id:1,
                    title:"tv",
                    price:200,
                },
                {
                    id:2,
                    title:"phone",
                    price:500,
                },
                {
                    id:3,
                    title:"laptop",
                    price:600,
                },
            ],
            country:''
        }
    },
    methods:{
        getTotal(){
            console.log('getTotal Method')
            return this.items.reduce((total,curr)=>(total = total + curr.price), 0)
        },
        changeFullName(){
            this.fullName = 'mohit bajaj'
        }
    },
    computed:{
        fullName:{
            get() {
                 return `${this.firstName} ${this.lastName}`
            },
            set(value){
                const names = value.split(' ')
                this.firstName = names[0]
                this.lastName = names[1]
            }  
        },
        total(){
            console.log('Total computed property')
            return this.items.reduce((total,curr)=>(total = total + curr.price), 0)
        },
        expensiveItems(){
            return this.items.filter(item =>item.price > 400)
        }
    }
}
</script>