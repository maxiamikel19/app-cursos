<template>
    <ul>
        <li v-for="item in lista" :key="item.id">
            {{ item.name }}
        </li>
    </ul>
</template>

<script>
    export default {
        name:'VLista',
        props:{
            lista : Array
        }
    }
</script>

<style lang="scss" scoped>

</style>