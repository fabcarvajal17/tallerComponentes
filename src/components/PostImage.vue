<template>
    <div class="post-image">
        <img src="" alt="">
    </div>
</template>

<script lang="ts">
    import { defineComponent, DefineComponent } from 'vue';
    export default defineComponent({
        name: "PostImage"
        props:{
            ruta:{
                type:String,
                default: ""
            }
        }
    })
</script>

<style lang="scss" scoped>

</style>