<template>
  <h1>PAR / ÍMPAR</h1>
  <div class="formulario">
    <label>Digite um número: </label>
    <input type="number" v-model="numero">
    <button @click="verificaNumero()">Verificar</button>
    <span class="resultado">{{ resultado }}</span>
  </div>
</template>

<script>
export default {
  data(){
    return{
      numero: 0,
      resultado: ""
    }
  },
  methods:{
    verificaNumero(){
      if (this.numero == 0 || this.numero == null){
        alert("Digite algum número!")
        return
      }

      if(this.numero % 2 == 0){
        this.resultado = "PAR"

      }else{
        this.resultado = "ÍMPAR"
      }
    }
  }
}
</script>

<style scoped>
h1{
  font-size: 30px;
  padding: 35px;
  text-align: center;
  color: blue;
}
.formulario{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.formulario input{
  width: 300px;
  height: 35px;
  outline: none;
  border: 2px solid blue;
  border-radius: 30px;
}

.resultado{
  margin-top: 30px;
  font-weight: 600;
}

button{
  width: 300px;
  height: 35px;
  margin-top: 30px;
  cursor: pointer;
  border-radius: 30px;
  border: 2px solid blue;
  background-color: blue;
  color: white;
}
</style>
