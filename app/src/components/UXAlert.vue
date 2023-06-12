<template>
    <div :class="baseClass">
        {{ text }}

        <button @click="onCLick()">
            X
        </button>
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
    },
    methods: {
        onCLick(){
            this.$emit('close')
            console.log('tste')
        }
    }
}


</script>

<style scoped>

button{
    border: none;
    background: none;
    cursor: pointer;
}
.alert{
    background: lightgray;
    color:black;
    font-size: larger;
    margin: 10px;
    padding: 30px;
    display: flex;
    justify-content: space-between;
}
.alert-sucess{
    background: skyblue;
}
.alert-danger{
    background: rgb(255, 70, 70);
}
</style>