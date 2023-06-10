<template>
    <header>
        <h1>
            <slot></slot> 
            <slot name="title"></slot> 
            <slot name="description"></slot> 
        </h1>
    </header>
</template>

<script>
    export default {
        name: 'App',
        data(){

        }
    }
</script>

<style>

header{
    background-color: blueviolet;
    color: aliceblue;
}
</style>