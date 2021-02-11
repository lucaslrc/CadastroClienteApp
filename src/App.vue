<template>
<div class="container-sm">
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">CadastroCliente</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                Menu
              </a>
              <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                <a class="dropdown-item" href="#">ListarClientes</a>
                <a class="dropdown-item" type="button" data-toggle="modal" data-target="#formModal">Adicionar Cliente</a>
              </div>
            </li>
          </ul>
        </div>
    </nav>
    <Clientes></Clientes>
    <CadastroCliente></CadastroCliente>
</div>
</template>

<script>
import Clientes from './components/Clientes.vue';
import CadastroCliente from './components/CadastroCliente.vue';

export default {
  name: 'App',
  components: {
    Clientes,
    CadastroCliente
  },
}
</script>

<style>

</style>
