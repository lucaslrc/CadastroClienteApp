<template>
    <div id="clientes">
        <table class="table">
            <thead>
                <tr>
                <th>ID</th>
                <th>Nome</th>
                <th>Nascimento</th>
                <th>Cep</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                <th scope="row"> {{ clientes.ID }}</th>
                <td>{{ clientes.nome }}</td>
                <td>{{ clientes.dataNascimento }}</td>
                <td>{{ clientes.cep }}</td>
                <div class="col-sm">
                    <button type="button" data-toggle="modal" data-target="#formModalCliente" class="btn btn-primary mr-1">Editar</button>
                    <button type="button" class="btn btn-danger">Remover</button>
                </div>
                </tr>
            </tbody>
        </table>
        <div class="modal fade" tabindex="-1" role="dialog" id="formModalCliente">
        <div class="modal-dialog" role="document">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title">Cliente</h5>
              <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                <span aria-hidden="true">&times;</span>
              </button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                  <label for="sexoDoCliente">Sexo</label>
                  <input type="text" class="form-control" id="sexoDoClienteId" readonly>
                </div>
                <div class="form-group">
                  <label for="sexoDoCliente">Sexo</label>
                  <input type="text" class="form-control" id="sexoDoClienteId"  readonly>
                </div>
                <div class="form-group">
                  <label for="sexoDoCliente">Sexo</label>
                  <input type="text" class="form-control" id="sexoDoClienteId"  readonly>
                </div>
            </div>
          </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
    name: 'Clientes',
    props: {
        clientes: Object
    }
}
</script>

<style scoped>

</style>