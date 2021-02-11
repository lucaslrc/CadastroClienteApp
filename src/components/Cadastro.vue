<template>
    <div class="modal fade" tabindex="-1" role="dialog" id="formModal">
        <div class="modal-dialog" role="document">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title">Cadastrar Cliente</h5>
              <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                <span aria-hidden="true">&times;</span>
              </button>
            </div>
            <div class="modal-body">
                <form>
                  <div class="form-group">
                    <label for="NomeCliente">Nome</label>
                    <input type="email" class="form-control" id="Nome" aria-describedby="emailHelp" placeholder="Nome completo">
                  </div>
                  <div class="form-group">
                    <label for="DataNascimentoCliente">Data de nascimento</label>
                    <input type="date" class="form-control" id="DataNascimento">
                  </div>
                  <button type="submit" class="btn btn-primary">Cadastrar</button>
                </form>
            </div>
          </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Cadastro'
}
</script>
<style>

</style>