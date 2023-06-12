<template>
    <div :class="baseClass">
        {{ text }}
    </div>
</template>

<script>
export default{
    props: ['variant', 'text'],
    computed: {
        baseClass() {
            return [
                'alert',
                this.variant ? `alert-${this.variant}` : ''
            ]
        },
    }
}


</script>

<style scoped>
.alert{
    background: lightgray;
    color:black;
    font-size: larger;
    margin: 10px;
    padding: 30px;
}
.alert-sucess{
    background: skyblue;
}
.alert-danger{
    background: rgb(255, 70, 70);
}
</style>