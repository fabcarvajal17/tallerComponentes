<template>
    <h1>
        Listado de POSTS
    </h1>

    <div class="post-container">
        <post-card 
            v-for="post in posts" :key="post.title"
            :title="post.title"
            :summary="post.sumary"
            :text="post.text"
            :ruta-imagen="post.image"
        />
        <post-card/>
        <post-card/>
        <post-card/>


    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';
    import PostCard from './PostCard.vue';
    import datos from '@/assets/json/datos.json'

    export default defineComponent({
        name: 'PostContainer',
        components: {
            PostCard
        },
        data(){
            return {
                //title: "este es el titulo desde data",
                //sumary: "este es el texto desde data"
            }

        },
        computed: {
            posts: () =>{
                return datos.map((post:any)=>{
                    return post
                })
            }
        }
    })
</script>

<style lang="scss" scoped>
.post-container{
    width: 100%;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}
</style>