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
                <input type="text" class="form-control">
                <div class="form-text">Exemplo: Dev Javascript</div>
            </div>
        </div>

        <div class="row mt-2">
            <div class="col">
                <label class="form-label">Descrição</label>
                <textarea type="text" class="form-control"></textarea>
                <div class="form-text">Informe os detalhes da vaga</div>
            </div>
        </div>

        <div class="row mt-2">
            <div class="col">
                <label class="form-label">Salário</label>
                <input type="number" class="form-control">
                <div class="form-text">Informe o salário</div>
            </div>

            <div class="col">
                <label class="form-label">Modalidade</label>
                <select class="form-select">
                    <option value="1">Home office</option>
                    <option value="2">Presencial</option>
                </select>
                <div class="form-text">Informe onde as atividades serão realizadas</div>
            </div>

            <div class="col">
                <label class="form-label">Tipo</label>
                <select class="form-select">
                    <option value="1">CLT</option>
                    <option value="2">PJ</option>
                </select>
                <div class="form-text">Informe o tipo de contratação</div>
            </div>
        </div>

        <!-- enviar vaga -->
        <div class="row mt-3">
            <div class="col">
                <button type="submit" class="btn btn-primary">
                    Cadastrar
                </button>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
    name: 'PublicarVagas'
 }
</script>


<style>

</style>