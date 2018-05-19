<template>
    <div>
        <img src="../assets/logo.png">
        <Categoria v-bind:categoria="objeto"></Categoria>
    </div>
</template>

<script>
    import Categoria from '@/components/Categoria.vue'
    import Vue from 'vue'

    export default {
        name: 'categoria',
        props: {},
        data: function () {
            return {
                objeto: {}
            }
        },
        components: {
            Categoria
        },
        methods: {
            getCategorias: function () {
                Vue.http.get(`http://localhost:8081/categorias/1`).then((res) => {
                    // Depois que a requisição terminar, passamos o resultado para função dispatch que se encarregará de atualizar a mutation
                    this.objeto = res.data;
                });
            }
        },
        mounted: function () {
            this.getCategorias();
        }
    }
</script>
