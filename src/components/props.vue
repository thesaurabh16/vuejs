<template>
    <h2>
        hello {{name}} a.k.a {{ heroName }}
    </h2>
</template>

<script>
    export default {
        name:'props',
        props:['name','heroName']
    }
</script>

<style scoped>

</style>