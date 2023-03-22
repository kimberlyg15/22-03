<template>
    <form action="" @submit.prevent="receberDados">
        <laber for="nome">Nome:</laber>
        <input v-model="inputNome" type="text" name="" id="nome">
        <label for="email">Email:</label>
        <input v-model="inputEmail" type="text" name="email">
        <label for="msg">mensagem: </label>
        <textarea v-model="inputmensagem" name="mensagem" id="msg"></textarea>
        <button> Enviar</button>
    </form>
</template>
<script>
export default {
    data: () => {
        return{
            inputNome: "",
            inputEmail: "",
            inputmensagem: "" 

        }
    },
    methods: {
        receberDados(){
            const dados = {
                nome: this.inputNome,
                email: this.inputEmail,
                msg: this.inputmensagem,
            }
            this.$emit("enviarDados",dados)
        }
    }
}
</script>