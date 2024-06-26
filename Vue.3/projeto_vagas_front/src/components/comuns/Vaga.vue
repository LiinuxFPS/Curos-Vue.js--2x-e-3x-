<template>
    <div class="card">
        <div class="card-header bg-dark text-white">
            {{ titulo }}
        </div>
        <div class="card-body">
            <p>{{ descricao }}</p>
        </div>
        <div class="card-footer">
            <small class="text-muted">
                Sálario: R${{ salario }} | 
                Modalidade: {{ modalidade }} | 
                Tipo: {{ tipo }} | 
                Publicação: {{ publicacao }}
            </small>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Vaga',
        //props: ['titulo','descricao','salario','modalidade','tipo','publicacao']
        //Tipagem de props
        props:{ titulo: String,
                descricao: String,
                salario: [Number, String],//pode aceitar mais de uma tipagem
                modalidade: String,
                tipo: String,
                publicacao: String
        }
    }
</script>

<style>

</style>