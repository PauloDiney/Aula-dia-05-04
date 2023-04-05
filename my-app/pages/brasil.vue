<template>
    <UL>
        <li>Nome Comum: {{ this.info[0].name.nativeName.por.common}}</li>
        <li>Nome Oficial: {{ this.info[0].name.nativeName.por.official }}</li>
        <li>Nome da Modeda:  {{ this.info[0].currencies.BRL.name }}</li>
        <li>Simbulo da Moeda:{{ this.info[0].currencies.BRL.symbol }}</li>
        <li>Capital:{{ this.info[0].capital }}</li>
        <li>Região: {{ this.info[0].region }}</li>
        <li>Sub-Região:{{ this.info[0].subregion}}</li>
        <li>Paises que Fazem Fronteira:{{ this.info[0].borders }}</li>
    </UL>
    
</template>

<script>

 import { dataToEsm } from "@rollup/pluginutils";
import informa from "~/brasil.json"

export default{
    data(){
        return{
            info:informa,
            

        }
    }
}


</script>