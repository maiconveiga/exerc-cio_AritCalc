<script setup>
import { reactive } from 'vue';
import Cabecalho from './components/Cabecalho.vue';
import Calculadora from './components/Calculadora.vue';
import Resultado from './components/Resultado.vue';

const estado = reactive({
    n1: 0,
    n2: 0,
    sinal: '+',
})

const resultado = () => {
    const { sinal } = estado;
    switch (sinal) {
        case '+':
            return (parseFloat(estado.n1) + parseFloat(estado.n2)).toFixed(1);

        case '-':
            return (parseFloat(estado.n1) - parseFloat(estado.n2)).toFixed(1);

        case '/':
            return (parseFloat(estado.n1) / parseFloat(estado.n2)).toFixed(1);

        case '*':
            return (parseFloat(estado.n1) * parseFloat(estado.n2)).toFixed(1);

        default:
            return
    }
}

const a = (evento) => { estado.n1 = evento.target.value };
const b = (evento) => { estado.n2 = evento.target.value };
const s = (evento) => { estado.sinal = evento.target.value };

</script>

<template>
    <div class="container">
        <Cabecalho></Cabecalho>
        <Calculadora :a="a" :b="b" :s="s"></Calculadora>
        <Resultado :result="resultado"></Resultado>
    </div>
</template>

<style scoped>
.container{
    margin: 0 auto;
    text-align: center;
    max-width: 1024px;
    width: 80%;
}

 
</style>
