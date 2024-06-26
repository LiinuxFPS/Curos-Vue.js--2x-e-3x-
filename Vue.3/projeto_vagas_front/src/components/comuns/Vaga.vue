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
        //exemplo 1 props: ['titulo','descricao','salario','modalidade','tipo','publicacao']
        
        //Tipagem de props
        //exemplo 2
        /*props:{ titulo: String,
                descricao: String,
                salario: [Number, String],//pode aceitar mais de uma tipagem
                modalidade: String,
                tipo: String,
                publicacao: String
        }*/

        //exemplo 3
        //Validação de props (required e validator)
        props:{
            titulo:{
                type: String,
                required: true
            },
            descricao:{
                type: String,
                required: true
            },
            salario:{
                type: [Number,String],
                required: true
            },
            modalidade:{
                type: String,
                required: true
            },
            publicacao:{
                type: String,
                required: true
            },
        }
    }
</script>

<style>

</style>