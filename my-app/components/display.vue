<template>
    <main>
         <section class="resultado">{{ valor }}</section>
    </main>
</template>

<script>


export default {
    props: {
        valor: {
            required: true
        }
    }
}



</script>







<style scoped>

.resultado {
    
    width: 400px;
    height: 50px;
    justify-content: flex-end;
    align-items: center;
    display: flex;
    background-color: white;
    justify-items: center;
    flex-direction: row;
    flex-wrap: wrap;
    align-content: stretch;
    margin: auto;
    font-size: 30px;
    overflow: hidden;
    
}
</style>