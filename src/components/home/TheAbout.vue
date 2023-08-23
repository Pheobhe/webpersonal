<template>
    <div class="about">
        <div class="about__content">
            <div class="about__content__left">
                <img 
                class="about__content__left__img"
                src="../../assets/House1.png"
                />
            </div>
            <div class="about__content__right">
                <h3 class="about__content__right__title">Sobre mi</h3>
                <p class="about__content__right__text">
                    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Animi illo aliquid labore commodi quod obcaecati tempora.
                </p>
                <div class="about__content__right_ctrl">
                    <v-button-main
                           textoBtn="LinkedIn"
                           :color-fondo="color1"
                           :color-texto="color2"
                    /> 
                    <v-button-main
                            textoBtn="GitHub"
                            :color-fondo="color2"
                            :color-texto="color1"
                     /> 
                </div>
            </div>
        </div>
    </div>
</template>

<script>
 import VButtonMain from '@/components/base/VButtonMain.vue'
 //import { c1, c2 } from '@/components/_app.scss'
 import { c1, c2 } from '@/components/_app.scss?vue&type=style&index=0&lang=scss&module=1'
    export default {
        name: 'TheAbout',
        data: function(){ 
            return{
                color1: c1,
                color2: c2,  
        }
    },
        components:{
            VButtonMain
        }
    }
</script>

<style lang="scss" scoped>


@import '../_app.scss';
.about{
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 5em;
    padding-bottom: 5em;
    background: $color1;
    opacity: 0.95 ;
    &__content{
        
        width: 50%;
        display: flex;
        justify-content: center;
        align-items: center;

        &__left{
            width: 150 px;
            height: 200 px;
            border: 1px solid $color2;
            margin-right: 3em;

            &__img{ 
                width: 100%;
                height: 100%;
                position: relative;
                left: 20px;
                top: -20px;
             }
        }

       
        &__right{ 
            display: block;
            width: 50%;
            color: $color-white;
            &__title{
                font-family: $ff-primary;
                font-size: 20px;
                border-bottom: 1px solid $color2;
                margin-bottom: 1em;
                padding-bottom: 1em;
            }
            &__text{
                font-size: 15px;
                font-family: $ff-secondary;
                margin-bottom: 1.5em;
            }
        }
       
    }
}

</style>