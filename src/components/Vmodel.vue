<template>
    <div>
        <h2>v-model</h2>
        <input type="text" v-model="name">
    </div>
</template>

<script>
    export default {
        name:'Vmodel',
        data(){
            return {
                name:''
            }
        }
    }
</script>

<style scoped>

</style>