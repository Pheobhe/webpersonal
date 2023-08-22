<template>
    <div class="skills">
        <h3 class="skills__title">Mis Habilidades</h3>
        <p class="skills__text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Earum voluptate obcaecati sit eius, ut fuga libero.</p>
   
        <div class="skills__items">
                <div 
                class="skills__item"
                v-for="habilidad in habilidades" 
                :key="habilidad.id"   
                >
                <v-card-main 
                    :titulo="habilidad.titulo"    
                    :contenido="habilidad.contenido"
                    :color="habilidad.color"
                />

               </div>
        </div>
    </div>
</template>

<script>



import VCardMain from '@/components/base/VCardMain'
import { c3, c4, c5 } from '@/components/_app.scss'

    export default {
        name: 'TheSkills',
        data: function() {
            return{ c3, c4, c5,
                habilidades: [
                    {'id': 0, titulo: 'Fuerza', contenido:'algún contenido de fuerza', color: "#ff9f1a"},
                    {'id': 1, titulo: 'Valentía', contenido:'algún contenido de valentía', color: c3},
                    {'id': 2, titulo: 'Coraje', contenido:'algún contenido de coraje', color: c4},
                    {'id': 3, titulo: 'Determinación', contenido:'algún contenido de determinación', color: c5},
                ]
            }
        },
        components: {
            VCardMain
        }
    }    
</script>

<style lang="scss" scoped>

@import '../_app.scss';
    .skills{
        background: $color1;
        padding: 4em;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        &__title {
            font-family: $ff-primary;
            color: $color-white;
            margin-bottom: 1em;
            font-size: 24px ;
        }
        &__text{
            font-family: $ff-secondary;
            color: $color-white;
            margin-bottom: 1em;
        }
        &__items{
            display: grid;
            grid-template-columns: 400px 400px;
        }
       
      

    }

</style>