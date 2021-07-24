<template>
  <h1>App contador: {{ contador }}</h1>
  <ContadorUno />
  <ContadorAccion />
</template>

<script>
import { ref } from '@vue/reactivity'
import ContadorUno from './components/ContadorUno.vue'
import ContadorAccion from './components/ContadorAccion.vue'
import { provide } from '@vue/runtime-core';

export default {
  name: 'App',
  components: {
    ContadorUno,
    ContadorAccion
  },
  setup(){
    const contador = ref(0);

    provide('contador', contador);

    return{ contador }
  }
 
}
</script>

