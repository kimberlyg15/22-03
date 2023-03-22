<template>
    <div>
        <form  @submit.prevent="receberNome">
        <laber for="nome">Nome:</laber>
        <input v-model="inputNome" type="text" name="" id="nome">
        <button> Adicionar</button>
   </form>
        <ul>
            <li v-for="nome in nomes">{{ nome }}</li>
        </ul>
        
    </div>
</template>

<script>
export default {
    data: () => {
        return{
            inputNome: "",
            nomes: []

        }
    },
    methods: {
        receberNome(){
                 this.nomes.push(this.inputNome)
                 this.inputNome = "";
            
        }
    }
}
</script>

