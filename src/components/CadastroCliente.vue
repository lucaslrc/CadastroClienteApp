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
                    <label for="NomeCliente">Nome</label><br>
                    <input type="text" id="nomeCliente" placeholder="Nome completo" v-model="nome">
                  </div>
                  <div class="form-group">
                    <label for="DataNascimentoCliente">Data de nascimento</label><br>
                    <input type="date" id="dataNascimento" v-model="dataNascimento">
                  </div>
                  <div class="form-group">
                    <label for="SexoCliente">Sexo</label><br>
                      <select class="form-control form-control-sm" id="sexoCliente" v-model="sexo">
                        <option>Masculino</option>
                        <option>Feminino</option>
                        <option>Outro</option>
                      </select>
                  </div>
                  <div class="form-group">
                    <label for="CepCliente">Cep</label><br>
                    <input type="text" class="form-control" id="cepCliente" v-model="cep">
                  </div>
                  <div class="form-group">
                    <label for="DataNascimentoCliente">Endereço</label><br>
                    <input type="text" class="form-control" id="enderecoCliente" v-model="endereco" readonly>
                  </div>
                  <div class="form-group">
                    <label for="DataNascimentoCliente">Número</label><br>
                    <input type="text" class="form-control" id="numeroCliente" v-model="numero">
                  </div>
                  <div class="form-group">
                    <label for="DataNascimentoCliente">Complemento</label><br>
                    <input type="text" class="form-control" id="complementoCliente" v-model="complemento" readonly>
                  </div>
                  <div class="form-group">
                    <label for="DataNascimentoCliente">Bairro</label><br>
                    <input type="text" class="form-control" id="bairroCliente" v-model="bairro" readonly>
                  </div>
                  <div class="form-group">
                    <label for="DataNascimentoCliente">Estado</label>
                    <input type="text" class="form-control" id="estadoCliente" v-model="estado" readonly>
                  </div>
                  <div class="form-group">
                    <label for="DataNascimentoCliente">Cidade</label>
                    <input type="text" class="form-control" id="cidadeCliente" v-model="cidade" readonly>
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
  name: 'CadastroCliente',
  data() {
    return {
    nome: '',
    dataNascimento: Date,
    sexo: '',
    cep: '',
    endereco: '',
    numero: '',
    complemento: '',
    bairo: '',
    estado: '',
    cidade: ''
    }
  }
}
</script>
<style scoped>

</style>