<template>
    <button class="post-button">Ver detalles</button>
</template>

<script lang="ts">
     import {defineComponent } from 'vue';
    export default defineComponent({
        name: 'postButon'
    })
</script>
   
<style lang="scss" scoped>
    .post-button{
        background-color: aqua;
        border: solid 2px blue;
        padding: 3px;
        border-radius: 5px;
    }
</style>