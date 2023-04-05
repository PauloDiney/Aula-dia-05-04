<template>
    <form @submit.prevent="$e =>salvarAluno()">
        <input type="text" placeholder="nome" id="nome" v-model="nome">
        <input type="number" placeholder="idade" id="number" v-model="idade">
        <input type="text" placeholder="serie" id="serie" v-model="serie">
        <button>Salvar</button>
    </form>
    <hr>
    <ul v-for="(aluno,index) in this.dados">
    
        <li >Nome:{{ aluno.nome }} </li>
        <li >idade:{{ aluno.idade }}</li>
        <li>Serie:{{ aluno.serie }}</li>
        <button @click="$e =>deletar(index)">Deletar</button>
       
    </ul>

</template>


<script>

import aluno from "~/alunos.json"

export default{
    data(){
        return{
            dados:aluno,
            nome:"",
            idade:"",
            serie:""
            
            
        }
   
        
    },
    methods:{
        salvarAluno(){
            this.nome,
            this.idade,
            this.serie,
            this.dados.push({"nome":this.nome, "idade":this.idade, "serie":this.serie})
        },
        deletar(index){
            this.dados.splice(index, 1);
        }
    
    }
}



</script>