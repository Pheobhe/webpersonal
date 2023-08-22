<template>
    <div class="personal-data" >

        <div class="personal-data__left">

            <div class="personal-data__left__content">

            <span class="personal-data__left__content__text">Hola</span>

            <h3 class="personal-data__left__content__name">Soy Juan</h3>
            
            <p class="personal-data__left__content__description">
                Soy Lorena y vivo en un mundo lleno de hipocresía
            </p>

            <v-button-main
                textoBtn="Contactar"
                color-fondo="#212121"
                color-texto="#ff9f1a"
            
            /> 
            <!-- :color-fondo="color1"
            :color-texto="color2" -->
        </div>
          
    </div>

        <div class="personal-data__right" >
            <img 
            class="personal-data__right__img"
            src="../../assets/house22.png">

        </div>
     
    </div>
</template>

<script>
 
 
 import VButtonMain from '@/components/base/VButtonMain.vue'
 import { c1, c2 } from '@/components/_app.scss'

    export default {
        name:'ThePersonalData',
        components: {
             VButtonMain
        },
        data: function() {
            return { c1,c2,
               
                color1: c1,
                color2: c2,
               
                }
        }
    }
</script>

<style lang="scss" scoped>
  
    @import '../../components/_app.scss';
    

    .personal-data{
      
        display: flex;
     


        &__left{
            background: $color1;
            width: 60%;
            display: flex;
            justify-content: center;
            align-items: center;
            &__content{
                width: 300px;
                color: $color-white;

                &__text {
                    font-family: $ff-secondary;
                    font-size: 14px;
                    margin-bottom: 10px;
                }
                &__name{
                    font-family: $ff-primary;
                    font-size: 24px;
                    color: $color2;
                    margin-bottom: 10px ;
                }
                &__description{
                    font-family: $ff-secondary;
                    font-size: 15px;
                    margin-bottom: 2em;

                }
            }
 

        }
        &__right{
            background: $color2;
            width: 40%;
            &__img{
                width: 200px;
                position: relative;
                left: -100px;
             
            }
        }
    }

</style>