<template>
    <main>
        <display :valor="display" />
        <numeros @digitar="digitar" />
        <acoes @limpar="limpar" @somar="somar" @igual="igual" @menos='menos' />
    </main>
</template>

<script>



export default {
    data() {
        return {
            display: "",
            n1: "",
            n2: "",
            ifi: "",

        }
    },
    methods: {
        digitar(valor) {


            if (this.ifi === "resul") {
                this.limpar()
                this.ifi = ""
            }

            this.display = this.display + valor;

        },
        limpar() {
            this.display = "";
            this.n1 = ""
            this.n2 = ""
        },
        somar() {
            this.n1 = parseInt(this.display)
            this.display = ""
            this.ifi = "mais"

        },
        menos() {
            this.n1 = parseInt(this.display)
            this.display = ""
            this.ifi = "menos"

        },
        igual() {
            if (this.ifi === "mais") {
                this.n2 = parseInt(this.display)
                this.display = this.n1 + this.n2
                this.ifi = "resul"

            }
            if (this.ifi === "menos") {
                this.n2 = parseInt(this.display)
                this.display = this.n1 - this.n2
                this.ifi = "resul"
            }


        }





    }
}

</script>











<style scoped>
main {
    display: block;
    align-items: center;
    margin: auto;
    width: 500px;
    height: auto;
    background-color: rgb(240, 240, 240);

}

body {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    width: auto;
}
</style>