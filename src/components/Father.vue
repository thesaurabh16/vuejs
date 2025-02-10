<template>
    <div>
        parent component
        <button @click="showChild = !showChild">Toggle Child</button>
        <Son v-if="showChild" />
    </div>
</template>

<script>
import Son from './Son.vue'
    export default {
        components:{
            Son
        },
        name:'Father',
        data(){
            return{
                showChild:true,
            }
        },
        beforeCreate(){
            console.log('parent beforeCreate()')
        },
        created(){
            console.log('parent Created()')
        },
        beforeMount(){
            console.log('parent Beforemouted()')
        },
        mounted(){
            console.log('parent mounted()')
        },
        beforeUpdate(){
            console.log('parent beforeUpdate()')
        },
        updated(){
            console.log('parent update()')
        },
        beforeUnmount(){
            console.log('child beforeunmount()')
        },
        unmounted(){
            console.log('parent unmounted()')
        },
    }
</script>

<style scoped>

</style>