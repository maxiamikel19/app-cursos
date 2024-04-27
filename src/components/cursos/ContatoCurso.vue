<template>
    <div class="contato">
        <h2 class="main-title">{{ titulo }}</h2>
        <form action="">
        <div class="contato__form">    
           <div class="contato__form__input">
              <input type="text" autocomplete="OFF" name="email" placeholder="Email" class="contato__form__input__control">
            </div>
            <div class="contato__form__input">
                <textarea name="message" autocomplete="OFF" id="" cols="30" rows="10" class="contato__form__input__control"></textarea>
            </div>
            <div class="contato__form__input">
                <button class="contato__form__input__btn" @click.prevent="null" >Enviar</button>
            </div>            
        </div>
    </form>
    </div>
</template>

<script>
    export default {
        name:'ContatoCurso',
        props:{
            titulo: String
        }
    }
</script>

<style lang="scss" scoped>
    .contato{
        border: none;
        margin: 0 auto;
        width: 100%;
        &__form{
            border:none;
            margin: 0 auto;
            padding: 2em;
            display: flex;
            align-items: center;
            flex-direction: column;
            &__input{
                margin: 10px 0px;
                display: flex;
                align-items: center;
                justify-content: left;
                border: none;
                width: 50%;
                &__control{
                    border: solid 1px #999;
                    border-radius: 8px;
                    width: 90%;
                    padding: 1em;
                }
                &__btn{
                    color: #666;
                    font-weight: 800;
                    padding: .5em 1em;
                    border:  solid 1px #999;
                    border-radius: 5px;
                    cursor: pointer;
                    &:hover{
                        color: #000;
                        background: #999;
                    }
                }
            }
        }
    }
    @media screen and (max-width:968px) {
        .contato{
           width: 100%;  
           margin: 0 auto;
           &__form{
                width: 100%;
                &__input{
                    width: 100%;
                }
            }
        }  
    }  
        
</style>