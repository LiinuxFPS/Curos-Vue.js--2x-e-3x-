<template>
    <div class="h-100 p-5 bg-light border rounded-3">
        <h2>Pesquisar vagas</h2>
        <div class="row">
            <di class="col">
                <div class="form-group">
                <label for="">Título da vaga</label>
                <input type="text" class="form-control" 
                    placeholder="digite para fazer a busca">
                <small class="form-text text-muted">
                    Informe palavras relacionadas a vaga
                </small>
                </div>
            </di>
        </div>
        <div class="row">
            <div class="col">
                <button 
                    class="btn btn-outline-dark mt-2"
                    type="button">Buscar
                </button>
            </div>
        </div>
    </div>    
</template>

<script>
export default {
    name: 'PesquisarVaga'
}
</script>