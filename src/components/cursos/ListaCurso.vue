<template>
    <div class="cursos">
        <h1 class="main-title">{{titulo}} </h1>
        <div class="cursos__content">
            <v-lista :lista="listaCurso"/>
        </div>
    </div>
</template>

<script>
import VLista from '../base/VLista.vue'
    export default {
  components: { VLista },
        name:'ListaCurso',
        props:{
            titulo : String
        },
        data(){
            return{
                listaCurso:[
                    {id:1, name:'Analise e desenvolvimento de sistema'},
                    {id:2, name:'Siencia de gestão de conta'},
                    {id:3, name:'Programação e desenvolvimento de sistema com VUEjs'},
                    {id:4, name:'Analise e desenvolvimento de sistema orientado a mestrado'},
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>