<template>
    <div>
        <div class="divVagasFavoritas">
            <button class="btn btn-primary" 
                type="button" data-bs-toggle="offcanvas" 
                data-bs-target="#offcanvasRight" 
                aria-controls="offcanvasRight">Vagas Favoritas
            </button>
        </div>

        <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasRight" aria-labelledby="offcanvasRightLabel">
        <div class="offcanvas-header">
        <h5 id="offcanvasRightLabel">Vagas Favoritadas</h5>
        <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body">
        ...
        </div>
        </div>
    </div>
</template>

<script>
export default {
name:"VagasFavoritas"
}
</script>

<style scoped>
    .divVagasFavoritas{
        position: absolute;
        z-index: 1;
        top: 60px;
        right: 5px;
    }
</style>