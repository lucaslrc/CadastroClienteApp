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
                    <label for="nomeDoClienteFor">Nome</label><br>
                    <input type="text" id="nomeDoClienteId" placeholder="Nome completo" v-model="nome"><br>
                    <div class="alert alert-danger" role="alert" v-if="nome < 1">
                      Campo obrigatório.
                    </div>
                  </div>
                  <div class="form-group">
                    <label for="dataNascimentoDoClienteFor">Data de nascimento</label><br>
                    <input type="date" id="dataNascimentoDoClienteId" v-model="dataNascimento">
                    <div class="alert alert-danger" role="alert" v-if="dataNascimento.length < 7">
                      Campo obrigatório.
                    </div>
                  </div>
                  <div class="form-group">
                    <label for="sexoDoClienteFor">Sexo</label><br>
                      <select class="form-control form-control-sm" id="sexoDoClienteId" v-model="sexo">
                        <option>Masculino</option>
                        <option>Feminino</option>
                        <option>Outro</option>
                      </select>
                    <div class="alert alert-danger" role="alert" v-if="sexo < 1">
                      Campo obrigatório.
                    </div>
                  </div>
                  <div class="form-group">
                    <label for="cepDoClienteFor">Cep</label><br>
                    <input type="text" class="form-control" id="cepDoClienteId" v-model="cep">
                    <div class="alert alert-danger" role="alert" v-if="cep.length < 8">
                      Campo obrigatório.
                    </div>
                  </div>
                  <div class="form-group">
                    <label for="enderecoDoClienteFor">Endereço</label><br>
                    <input type="text" class="form-control" id="enderecoDoClienteId" v-model="endereco" readonly>
                  </div>
                  <div class="form-group">
                    <label for="numeroDoClienteFor">Número</label><br>
                    <input type="text" class="form-control" id="numeroDoClienteId" v-model="numero">
                  </div>
                  <div class="form-group">
                    <label for="complementoDoClienteFor">Complemento</label><br>
                    <input type="text" class="form-control" id="complementoDoClienteId" v-model="complemento" readonly>
                  </div>
                  <div class="form-group">
                    <label for="bairroDoClienteFor">Bairro</label><br>
                    <input type="text" class="form-control" id="bairroDoClienteId" v-model="bairro" readonly>
                  </div>
                  <div class="form-group">
                    <label for="estadoDoClienteFor">Estado</label>
                    <input type="text" class="form-control" id="estadoDoClienteId" v-model="estado" readonly>
                  </div>
                  <div class="form-group">
                    <label for="cidadeDoClienteFor">Cidade</label>
                    <input type="text" class="form-control" id="cidadeDoClienteId" v-model="cidade" readonly>
                  </div>
                  <button type="button" class="btn btn-primary" @click="cadastrarCliente">Cadastrar</button>
                </form>
            </div>
          </div>
        </div>
    </div>
</template>

<script>
import fetch from 'node-fetch';

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
    bairro: '',
    estado: '',
    cidade: ''
    }
  },
  methods: {
    cadastrarCliente() {
      // let infos = [''];
      // if (this.nome == '' || this.nome == '  ' || String.length(this.nome) < 1) {
        
      // }
    },
    buscarCep: (cep) => {
      console.log(cep);
      fetch('https://viacep.com.br/ws/' + cep + '/json/')
        .then(res => console.log(res))
    }
  }
}
</script>
<style scoped>

</style>