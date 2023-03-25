<script setup>
import ImprimirFecha from './components/ImprimirFecha.vue'
</script>

<template>
  <header>
    <h1>aplicacion fecha</h1>
  </header>

  <div>
    <input type="number" v-model="imputdia" placeholder="dia" />
    <input type="number" v-model="imputmes" placeholder="mes" />
    <input type="number" v-model="imputaño" placeholder="año" />
  </div>
  <div>
    <button @click="esactivo">enviar</button>
  </div>
  <div v-if="activo">
    <ImprimirFecha :dia="imputdia" :mes="imputmes" :año="imputaño" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      imputdia: '',
      imputmes: '',
      imputaño: '',
      activo: false
    }
  },
  methods: {
    esactivo() {
      this.activo = true
    }
  }
}
</script>
<style scoped></style>
