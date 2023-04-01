<template>
  <div>
    <h1>App Contador: {{ contador }}</h1>
    <ContadorUno/>
    <contadorAccion/>
  </div>
</template>


<script>
import { provide, ref } from 'vue'
import ContadorUno from './components/ContadorUno.vue';
import ContadorAccion from './components/ContadorAccion.vue';
export default {
  components: {
    ContadorUno,
    ContadorAccion

  },
  setup(){
    const contador = ref(0);

    provide('contador', contador) // puede ser accedido a cualquier componente secundario

    return {
      contador
    }
  }
}
</script>
