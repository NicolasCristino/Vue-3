<template>
    <div>
        <h1 :class="{'title' : true, 'title-home': isHome }">
            Curso Vue 3
        </h1>
        
        <p :class="['title', 'text']">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit, est ab. Reprehenderit ab rerum, amet, accusamus cupiditate dolor magnam quibusdam eius molestias corporis ut eaque voluptate veritatis facere voluptatum quos?
        </p>

        <p :class="['title', {'react': isHome}]">
            Reatividade
        </p>
        
        <p :style="{'color' : 'red'}">
            Style
        </p>

        <img v-bind:src="imagem" v-bind:alt="fotoDesc">
    </div>
</template>

<script>
    export default {
        name: 'App',
        data(){
            return{
                fotoDesc: 'ImagemPlaceholder',
                imagem: 'https://placehold.co/600x400',
                classVar: 'title',
                isHome: false,
                todos:[
                    {
                        "userId": 1,
                        "id": 1,
                        "title": "delectus aut autem",
                        "completed": false
                    },
                    {
                        "userId": 1,
                        "id": 2,
                        "title": "quis ut nam facilis et officia qui",
                        "completed": false
                    },
                    {
                        "userId": 1,
                        "id": 3,
                        "title": "fugiat veniam minus",
                        "completed": false
                    },
                    {
                        "userId": 1,
                        "id": 4,
                        "title": "et porro tempora",
                        "completed": true
                    },
                    {
                        "userId": 1,
                        "id": 5,
                        "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
                        "completed": false
                    }
                    ]
            }
        }
    }
</script>

<style>
    .todos_list{
        background: black;
        margin: 0 0 5px 0;
        padding: 3px 6px;
        color: #fff;
    }
    .title{
        color: purple;
    }
    .title-home{
        color: red;
        font-size: larger;
    }
    .text{
        color: black;
    }
    .react{
        color: chartreuse;
        font-weight: 900;
    }
</style>