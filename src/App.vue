<template>
<div class="container-fluid">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="/">CadastroCliente</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
        <ul class="navbar-nav">
            <li class="nav-item">
              <button type="button" class="btn btn-info" @click="listarClientes">Listar Clientes</button>
            </li>
            <li class="nav-item">
              <button type="button" class="btn btn-success" data-toggle="modal" data-target="#formModal">Cadastrar Cliente</button>
            </li>
        </ul>
    </nav>
    <CadastroCliente/>
    <Clientes :clientes="newCliente"/>
</div>
</template>

<script>
import CadastroCliente from './components/CadastroCliente.vue';
import Clientes from './components/Clientes.vue';
import fetch from 'node-fetch';

export default {
  name: 'App',
  components: {
    CadastroCliente,
    Clientes
  },
  data() {
    return {
      newCliente: {
        id: Number,
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
    }
  },
  methods: {
    listarClientes: function() {
      fetch('https://localhost:5000/api/CadastroCliente/ListarClientes', {
          method: 'GET',
          headers: {
            'Content-Type': 'application/json'
          },
          mode: 'cors'
        }).then(res => res.json())
          .then(result => {
            for (let i = 0; i < result.length; i++) {
              this.newCliente.ID = result[i].ID
              this.newCliente.nome = result[i].Nome
              this.newCliente.dataNascimento = result[i].DataNascimento
              this.cep = result[i].Cep
            }
          })
    }
  }
}
</script>

<style>

</style>
