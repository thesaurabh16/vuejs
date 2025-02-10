<template>
    <h1>Home Page{{ "Hello".length }}</h1>
    <h1>Email:- {{ emails }}</h1>
    <h1>NUMBER:- {{ phone }}</h1>
    <h1>Name:- {{ getName() }}</h1>
    <h1>Name:- {{ getNames("cloud") }}</h1>
    <h1>Address:- {{ getAddress() }}</h1>
    <h1>Address1 {{ getAddres("pokhara") }}</h1>
    <h1>Address2 {{ getAddres("Birgunj") }}</h1>
    <h1>Old data {{ getData() }}</h1>
    <h1>Old data {{ getData().name }}</h1>
    <h1>Old data {{ getDatas().email }}</h1>
    <input type="text" v-model="count"/>
    <h2>{{ count }}</h2>
    
</template>

<script>
export default {
    name:'HomePage',
    
    data(){
        return{
            count:10,
            emails:"cloudtech@gmail.com",
            phone:-9999,
            getName:function()
            {
                return "cloud tech"
            },
            getNames:function(a)
            {
                return a;
            }
        }
    },
    methods:{
        getAddress(){
            return "Kathmandu"
        },
        getAddres(detail){
            return detail;
        },
        getData(){
            return{
                name:'aviraj',
                email:'aviraj@gmail.com'
            }
        },
        getDatas(){
            return{
                name:'aviraj',
                email:this.emails
            }
        },
        
    }
}
</script>