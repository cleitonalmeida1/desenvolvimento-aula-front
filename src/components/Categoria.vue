<template>
    <table>
        <thead>
        <tr>
            <th>ID</th>
            <th>Nome</th>
        </tr>
        </thead>
        <tbody>
        <!-- For do vue para a propriedade passada -->
        <tr>
            <td>{{categoria.id}}</td>
            <td>{{categoria.nome}}</td>
        </tr>
        </tbody>
    </table>
</template>


<script>
    export default {
        // declaração das propriedade que o componente irá receber
        name: 'Categoria',
        props: {
            categoria: Object
        }
    }
</script>

<style scoped>

</style>