<template>
   <a
    class="main-btn"
    href="#"
    :style="{background: colorFondo, color: colorTexto}">
    {{ texto }}
   </a>

</template>

<script>
    export default {
        name: 'VButtonMain',
        props: {
            texto: String,
            colorTexto: String,
            colorFondo: String
        }
    }
</script>

<style lang="scss" scoped>

@import '../_app.scss';
    .main-btn{
        padding: 7px 15px 7px 15px;
        font-family: $ff-secondary;
        border: 1px solid;
        margin: 5px;


    }
</style>