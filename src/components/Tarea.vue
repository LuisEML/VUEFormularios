<template>
    <div>
        Estas en la pagina 
        <slot></slot>
    </div>
</template>


<script>
    export default{
        name:'Tarea'
    }
</script>

<style scoped>
    :slotted(img){
        width: 395px;
        height: 295px;
    }
</style>