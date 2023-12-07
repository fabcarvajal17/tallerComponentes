<template>
  <div class="post-card">
    <h1>{{title}}</h1>
    <p>
      {{summary}}
    </p>
    <post-image :ruta="rutaImagen">
    <post-button/>
  </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';
    import PostButton from './PostButton.vue'
    import PostImage from './PostImage.vue';

    export default defineComponent({
        name: 'post-card',
        components:{
            PostButton, PostImage
        },
        props:{
            title: {
                type: String,
                default:"",
            },
            summary: {
                type: String,
                default: "",
            },
            text: {
                type: String,
                default: "",
            },
            rutaImagen:{
                type: String,
                default:""
            }
        }
    })
</script>

<style lang="scss" scoped>
    .post-card{
        border-radius: 15px;
        padding: 10px;
        margin: 5px;
        border: solid 1px #ccc;
        min-width: 80%;
    }
</style>