<template>
    <div class="container py-4">
        <div class="row">
            <div class="col">
                <h3>Publicar Vagas</h3>
            </div>
        </div>
        <!-- cadastrar vaga -->
        <div class="row mt-2">
            <div class="col">
                <label class="form-label">Título da vaga</label>
                <input type="text" class="form-control" v-model="titulo">
                <div class="form-text">Exemplo: Dev Javascript</div>
            </div>
        </div>

        <div class="row mt-2">
            <div class="col">
                <label class="form-label">Descrição</label>
                <textarea type="text" class="form-control" v-model="descricao"></textarea>
                <div class="form-text">Informe os detalhes da vaga</div>
            </div>
        </div>

        <div class="row mt-2">
            <div class="col">
                <label class="form-label">Salário</label>
                <input type="number" class="form-control" v-model="salario">
                <div class="form-text">Informe o salário</div>
            </div>

            <div class="col">
                <label class="form-label">Modalidade</label>
                <select class="form-select" v-model="modalidade">
                    <option value="" disabled>Selecionar</option>
                    <option value="1">Home office</option>
                    <option value="2">Presencial</option>
                </select>
                <div class="form-text">
                    Informe onde as atividades serão realizadas
                </div>
            </div>

            <div class="col">
                <label class="form-label">Tipo</label>
                <select class="form-select" v-model="tipo">
                    <option value="" disabled>Selecionar</option>
                    <option value="1">CLT</option>
                    <option value="2">PJ</option>
                </select>
                <div class="form-text">Informe o tipo de contratação</div>
            </div>
        </div>
        
        <!-- enviar vaga -->
        <div class="row mt-3">
            <div class="col">
                <button type="submit" class="btn btn-primary"
                    @click="salvarVaga()">
                    Cadastrar
                </button>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'PublicarVagas',
        data:()=>({

            //fazer um v-model para realizar um two-way data-binding
            titulo:'',
            descricao:'',
            salario:'',
            modalidade:'',
            tipo:''
        }),
        methods:{
            salvarVaga(){

                //converte a string em objeto para resgatar os atributos
                let vagas = JSON.parse(localStorage.getItem('vagas'))

                if(!vagas) vagas = []

                let vaga ={
                    titulo: this.titulo,
                    descricao: this.descricao,
                    salario: this.salario,
                    modalidade: this.modalidade,
                    tipo: this.tipo
                }
                vagas.push(vaga)
                //transforma o objeto vaga em uma string
                localStorage.setItem('vagas',JSON.stringify(vagas))
                //console.table(vaga)
            }
        }
    }
</script>


<style>

</style>