<template>
    <main>
        <section class="button">
            <div class="pula">
                <button @click="($e) =>$emit('digitar', 7)">7</button>
                <button @click="($e) =>$emit('digitar', 8)">8</button>
                <button @click="($e) =>$emit('digitar', 9)">9</button>
            </div>
            <div class="pula">
                <button @click="($e) =>$emit('digitar', 4)">4</button>
                <button @click="($e) =>$emit('digitar', 5)">5</button>
                <button @click="($e) =>$emit('digitar', 6)">6</button>
            </div>
            <div class="pula">
                <button @click="($e) =>$emit('digitar', 1)">1</button>
                <button @click="($e) =>$emit('digitar', 2)">2</button>
                <button @click="($e) =>$emit('digitar', 3)">3</button>
            </div>
            <div class="pula">
                <button @click="($e) =>$emit('digitar', 0)">0</button>
               
            </div>
        </section>
    </main>
</template>

<style scoped>
  .button {
    display: flex;
    flex-wrap: wrap;
    margin-top: 5px;
    align-items: center;
    justify-content: center;
    
    flex-direction: column;

}

.button button {
    width: 50px;
    height: 50px;
    background-color: #004aad;
    padding: 10px;
    border-color: white;
    font-size: 30px;
}

.button :hover{
    background-color: white;
    color: #004aad;
}


.pula {
    display: flex;
   justify-content: center ;
   align-items: center;
   flex-direction: row;
    
}


</style>