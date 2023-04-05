<template>
   <main>
    <section class="acoes">
            <button @click="$emit ('somar')">+</button>
            <button @click="$emit('menos')">-</button>
            <button @click="$emit ('igual')">=</button>
            <button @click="$emit ('limpar')">C</button>
        </section>
   </main>
</template>


<style scoped>
.acoes {
    background-color:rgb(240, 240, 240);
    padding: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 30px;
}

.acoes button {
    width: 50px;
    height: 50px;
   background-color: #004aad;
    font-size: 16px;
    border-color: white;
    font-size: 30px;
    
}

.acoes :hover{
    background-color: white;
    color: blue;
}


</style>