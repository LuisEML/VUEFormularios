<template>
    <App>
        <h1>{{titulo}}</h1>
        <slot></slot>
    </App>
</template>

<script>
    export default{
        props:['titulo','parrafo']
    }
</script>