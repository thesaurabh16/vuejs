<template>
<h3 v-for="name in names" :key="name.firstName">
  <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
</h3>
</template>
<script>
export default{
    name:'Slots',
    data(){
        return{
            names:[
                {
                    firstName:"Saurabh",
                    lastName:"Shah",
                },
                {
                    firstName:"Gautam",
                    lastName:"Gupta",
                },
                {
                    firstName:'Aviraj',
                    lastName:'Gupta'
                },
            ],
        }
    }
}
</script>