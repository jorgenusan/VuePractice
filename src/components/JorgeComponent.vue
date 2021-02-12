<template>
  <div id="jorge">
    <h1>Primer componente.</h1>
    <span>{{texto}}</span>
    <input v-model="message" placeholder="Nombre">
    <button v-on:click="contar">Contar</button>
    <p>El número de letras que tiene tu nombre es: {{count}}</p>
  </div>
</template>

<script>
export default {
  name: "JorgeComponent",
  data(){
    return{
      texto:"Introduce tu nombre para contar las letras del mismo:",
      message:"",
      count:0
    }
  },

  methods:{
    contar(){
      this.count = this.message.split('').length
    }
  }
}
</script>

<style scoped>
  button{
    margin: 10px;
  }
  input{
    margin-left: 10px;
  }
  #jorge{
    margin-top: 5em;
  }
  h1{
    text-decoration: cadetblue;
    font-weight: bold;
  }
</style>