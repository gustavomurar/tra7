<script setup>
import {reactive, ref} from 'vue'

const produto= reactive({
  nome: '',
  idade: 1,
  senha: '',
  consenha: '',
  cidade: '',
z})

const mostraResultado= ref(false)


</script>

<template>
  <h1>{{ titulo }}</h1>
  <div class="contanier">
    <div class="formulario">
      <h2>Dados pessoais:</h2>

      <form @submit.prevent="mostraResultado = !mostraResultado">
      <div class="row">
        <label for="">Nome:</label>
        <input type="text" v-model="produto.nome" required/>
      </div>

      <div class="row">
        <label for="">Idade:</label>
        <input type="number" v-model="produto.preco"/>
      </div>

      <div class="row">
        <label for="">Senha:</label>
        <input type="password" v-model="produto.senha" />
      </div>

      <div class="row">
        <label for="">Confirmar senha:</label>
        <input type="password" v-model="produto.consenha" />
      </div>

      <div class="row">
        <label for="">Email:</label>
        <input type="email" v-model="produto.email" />
      </div>


      <div class="row">
        <label for="">Data de nascimento:</label>
        <input type="date" v-model="produto.consenha" />
      </div>

      <div class="row">
        <label for="">Cidade:</label>
        <input type="string" v-model="cidade" />
      </div>

      <div class="row">
        <label for="">Estado:</label>
        <input type="select" v-model="estado" />
      </div>

      <div class="row">
        <label for="">Hobbies:</label>
        <input type="text" v-model="nome" autocomplete="on" />
      </div>

      <div class="row">
        <label for="">Biografia:</label>
        <input type="text" v-model="nome" autocomplete="on" />
      </div>

      <div class="row">
        <label for="">Estado:</label>
        <input type="select" v-model="nome" autocomplete="on" />
      </div>
      
      </form>
    </div>

    
  </div>
</template>

<style scoped>

.contanier{
display: flex;
flex-direction: row;
justify-content: center;
gap: 1.5rom;
width: 100w;
}

.formulario,
.resultado {
  background-color:rgb(255, 255, 255);
  border-radius: 10px;
  padding: 10px;
}

.formulario{
  background-color:rgba(201, 181, 70, 0.699);
}

.formulario.row{
  margin: 10px auto;
  width: 70%;
  display: flex;
  justify-content: space-between;
}

.resultado{
  background-color:rgb(224, 131, 236);
}


</style>