<template>
    <ul class="lista">
        <li v-for="item in lista" :key="item.id" class="lista__item">
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
    .lista{
        border: none;
        margin: 2em;
        &__item{
            list-style:armenian;
            margin: 1em 0em;
        }
    }
</style>