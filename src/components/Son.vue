<template>
    <div>
        Child Component
    </div>
</template>

<script>
    export default {
        name:'Son',
        beforeCreate(){
            console.log('child beforeCreate()')
        },
        created(){
            console.log('child Created()')
        },
        beforeMount(){
            console.log('child Beforemouted()')
        },
        mounted(){
            console.log('child mounted()')
        },
        beforeUpdate(){
            console.log('child beforeUpdate()')
        },
        updated(){
            console.log('child update()')
        },
        beforeUnmount(){
            console.log('child beforeunmount()')
        },
        unmounted(){
            console.log('child unmounted()')
        },
    }
</script>

<style scoped>

</style>