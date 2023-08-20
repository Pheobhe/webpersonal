<template>
    <div class="skills">
        <h3 class="skill__title">Mis Habilidades</h3>
        <p class="skill__text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Earum voluptate obcaecati sit eius, ut fuga libero. Veniam, officia? Perspiciatis quaerat cupiditate quod vitae sint sunt facere eum soluta minus labore?</p>
   
        <div class="skill_items">
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
 import {c2, c3, c4, c5 } from '@/components/_app.scss'
// $c2: orange;
// $c3: blue;
// $c4: c56cf0;
// $c5: 3ae374;

    export default {
        name: 'TheSkills',
        data() {
            return{
                habilidades: [
                    {'id': 0, titulo: 'Fuerza', contenido:'algún contenido', color: c2},
                    {'id': 1, titulo: 'Valentía', contenido:'algún contenido', color: c3},
                    {'id': 2, titulo: 'Coraje', contenido:'algún contenido', color: c4},
                    {'id': 3, titulo: 'Determinación', contenido:'algún contenido', color: c5}
                ]
            }
        },
        components: {
            VCardMain
        }
    }    
</script>

<style lang="scss" scoped>

</style>