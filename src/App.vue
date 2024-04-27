<template>
    <div class="app">
      <div class="app__nav-menu">
        <h2 class="app__nav-menu__title">App cursos</h2>
        <ul class="app__nav-menu__menu">
          <li class="app__nav-menu__menu__item">
            <a href="" class="app__nav-menu__menu__item__link">Professores</a>
          </li>
          <li class="app__nav-menu__menu__item">
            <a href="" class="app__nav-menu__menu__item__link">Cursos</a>
          </li>
          <li class="app__nav-menu__menu__item">
            <a href="" class="app__nav-menu__menu__item__link">Contato</a>
          </li>
        </ul>
      </div>
    </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style lang="scss">
  *{
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
  }

  .app{
    border-bottom: solid 2px #eee;
    &__nav-menu{
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0em 1em;
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
</style>
