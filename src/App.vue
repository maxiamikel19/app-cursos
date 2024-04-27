<template>
    <div class="app">
      <div class="app__nav-menu">
        <h2 class="app__nav-menu__title">App cursos</h2>
        <ul class="app__nav-menu__menu">
          <li class="app__nav-menu__menu__item">
            <a href="" class="app__nav-menu__menu__item__link" @click.prevent="toggleMenu('lista-professor', 'Lista de professores')">Professores</a>
          </li>
          <li class="app__nav-menu__menu__item">
            <a href="" class="app__nav-menu__menu__item__link" @click.prevent="toggleMenu('lista-curso', 'Lista de cursos')">Cursos</a>
          </li>
          <li class="app__nav-menu__menu__item">
            <a href="" class="app__nav-menu__menu__item__link" @click.prevent="toggleMenu('contato-curso', 'Contatos')">Contato</a>
          </li>
        </ul>
      </div>
    </div>
    <div class="container">
      <!-- <lista-curso titulo="Lista de cursos"/>
      <lista-professor titulo="Lista de professores" />
      <contato-curso titulo="Contactos" /> -->
      <keep-alive>
        <component 
          :is="compoentSelected"
          :titulo="propComponent"
       />
      </keep-alive>
      
    </div>
</template>

<script>
import ContatoCurso from './components/cursos/ContatoCurso.vue'
import ListaCurso from './components/cursos/ListaCurso.vue'
import ListaProfessor from './components/cursos/ListaProfessor.vue'

export default {
  name: 'App',
  components: {
    ListaCurso,
    ListaProfessor,
    ContatoCurso,
  },
  data(){
    return{
      // professorList : ListaProfessor,
      // courseList : ListaCurso,
      // contact : ContatoCurso,
      compoentSelected: null,
      propComponent: ''
    }
  },
  methods:{
    toggleMenu: function (content, property){
      this.compoentSelected = content;
      this.propComponent = property;
    }
  }
}
</script>

<style lang="scss">
  *{
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
  }
  .main-title{
    color: #999;
    text-align: center;
    font-size: 20px;
    text-transform: uppercase;
  }

  .app{
    border-bottom: solid 2px #eee;
    &__nav-menu{
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 1em 1em;
      &__title{
        font-size: 18px;
        color: #666;
      }
      &__menu{
        display: flex;
        align-items: center;
        justify-content: center;
        &__item{
          list-style: none;
          margin: 10px;
          &__link{
            color:#666;
            text-decoration: none;
            &:hover{
              padding-bottom: 10px;
              border-bottom: solid 2px red;
            }
          }
        }
      }
    }
  }

  .container{
    padding: 2em;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    border: none;
  }
</style>
