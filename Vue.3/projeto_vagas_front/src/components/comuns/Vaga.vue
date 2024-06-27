<template>
    <div class="card">
        <div class="card-header bg-dark text-white">
            {{ titulo }}
        </div>
        <div class="card-body border border-secondary">
            <p>{{ descricao }}</p>
        </div>
        <div class="card-footer bg-secondary border border-secondary">
            <small class="text-dark">
                Sálario: R${{ salario }} | 
                Modalidade: {{ getModalidade }} | 
                Tipo: {{ getTipo }} | 
                Publicação: {{ getPublicacao }}
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
            tipo:{
                type: String,
                required: true
            },
            publicacao:{
                type: String,
                required: true
            },
        },
        computed:{
            getModalidade(){
                switch(this.modalidade){
                    case '1' : return 'Home Office'
                    case '2' : return 'Presencial'
                }
                return ''
            },
            getTipo(){
                switch(this.tipo){
                    case '1' : return 'CLT'
                    case '2' : return 'PJ'
                }
                return ''
            },
            getPublicacao(){
                let dataPublicacao = new Date(this.publicacao)
                return dataPublicacao.toLocaleString()
            }
        }
    }
</script>

<style>

</style>