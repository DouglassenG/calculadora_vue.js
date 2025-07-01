<script setup>
import { reactive, computed } from 'vue';

const estado = reactive({
  valor1: 0,
  valor2: 0,
  filtro: 'adicao',
});

const resultado = computed(() => {
  const { valor1, valor2, filtro } = estado;
  const n1 = parseFloat(valor1);
  const n2 = parseFloat(valor2);

  if (isNaN(n1) || isNaN(n2)) return '';

  switch (filtro) {
    case 'adicao':
      return n1 + n2;
    case 'subtracao':
      return n1 - n2;
    case 'multiplicacao':
      return n1 * n2;
    case 'divisao':
      return n2 !== 0 ? (n1 / n2).toFixed(2) : 'Erro: divisão por zero';
    default:
      return '';
  }
});
</script>

<template>
  <div class="container">
    <header class=" p-5 mb-4 mt-4 bg-info text-dark rounded-4">
      <h1>Calculadora</h1>
    </header>
    <div class="p-4 row bg-success rounded-4 text-light">
      <h3>Escolha um operador abaixo</h3>
      <div class="col-md-5">
        <select v-model="estado.filtro" class="form-control mb-4">
          <option value="adicao">(+) Somar</option>
          <option value="subtracao">(-) Subtrair</option>
          <option value="multiplicacao">(*) Multiplicar</option>
          <option value="divisao">(/)Dividir</option>
        </select>
      </div>
      <div class="col">
        <input class="form-control mb-2" type="number" v-model="estado.valor1" placeholder="Valor 1" />
        <input class="form-control mb-2" type="number" v-model="estado.valor2" placeholder="Valor 2" />

        <div class="mt-4">
          <h3>=   {{ resultado }}</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
h1 {
  text-align: center;
}
</style>
