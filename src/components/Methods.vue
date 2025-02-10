<template>
    <h2>methods</h2>
<h2>add methods - {{ add(10,20,21) }}</h2>
<h2>add methods - {{ add(1,2,11) }}</h2>
<h2>multiply methods - {{ multiply(21) }}</h2>
<h2>multiply methods - {{ multiply(baseValue) }}</h2>
</template>

<script>
export default {
    name:'Methods',
    data(){
        return{
            baseMultiplier:5,
            baseValue:2
        }
    },
    methods:{
        add(a,b,c){
            return a + b+ c
        },
        multiply(num){
            return num * this.baseMultiplier
        }
    }
}
</script>