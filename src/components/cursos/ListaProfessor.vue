<template>
    <div class="professor">
        <h1 class="main-title">{{ titulo }}</h1>
        <div class="professor__content">
            <v-lista :lista="listaProfessor"/>
        </div>
    </div>
</template>

<script>
import VLista from '../base/VLista.vue'
    export default {
  components: { VLista },
        name:'ListaProfessor',
        props:{
            titulo: String
        },
        data(){
            return{
                listaProfessor:[
                    {id:1, name:'Amikel Maxi Celestio Benoît'},
                    {id:2, name:'Myrlande Louissaint Maxi'},
                    {id:3, name:'Jerry Russell Alberto Maxi Jeudy'},
                    {id:4, name:'Karen Jenifer Maxi Pierre'},
                    {id:4, name:'Jesus Adrian Romeo'},
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>