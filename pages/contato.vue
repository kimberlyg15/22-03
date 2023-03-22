<template>
    <h1>
        pagina de contato</h1> 
       <FormularioContato 
       @enviarDados="receberDados"
       />
       <hr>
       <p>lista de contatos:</p>

       <ul v-for="ct in Object.keys(listaContato)">
        <li> nome: <strong>{{listaContato[ct].nome}}</strong></li>
        <li> email: <strong>{{listaContato[ct].email}} </strong></li>
        <li> mensagem:<strong> {{listaContato[ct].msg}} </strong></li>
        <hr>
       </ul>
    
</template>

<script>
export default {
data(){
    return{
        listaContato:[]
     }
  },
  methods: {
    receberDados (dados){
        console.log(dados)
        this.listaContato.push(dados)
    }
  }
}
</script>

