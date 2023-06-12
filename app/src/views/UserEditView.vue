<template>
    <div>
        <button @click="enviar()">
            Submit
        </button>
        <pre>
            {{ $route }} <!--Objeto de todo o esquema de roteamento-->>
        </pre>
    </div>
</template>

<script>
export default {
    created(){
        console.log(this.$route) // Objeto da rota ATUAL
    },
    methods: {
        enviar(){
            console.log('deu')
            this.$router.push('/about')
        }
    }
}
</script>