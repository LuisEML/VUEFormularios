<!-- <template>
    <Grid>
        <img v-bind:src="url" :alt="nombre">
        <h2>{{ nombre }}</h2>
        <a :href="url" target="_blank">Descargar</a>
        <a :href="nombre" target="_blank">Visitar</a>
        <contador></contador>
    
    </Grid>
</template>
<script>
     import Grid from "./Grid.vue"
    export default{
        props:{
            url:{
                String,
            },
            nombre:{
                String,
            }
        },
         components: {Grid}
    }
</script> -->

<style scoped>
 
    img{
        width: 8rem;
        padding: 0.5rem;
        background: snow;
    }
    a{
        text-decoration: none;
        color: snow;
        background: #301675;
        padding: 0.3rem;
        border-radius: 5px;
        border: 1px solid #f2f2f2;
    }
</style>