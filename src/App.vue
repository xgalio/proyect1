<script setup>
import ImprimirFecha from './components/ImprimirFecha.vue'
import Eliminar from './components/Eliminar.vue';

</script>

<template>
  <header>
    <h1>aplicacion fecha</h1>
  </header>

  <div>
     <!-- Seria los inputs  -->
    <input type="number" v-model="imputdia" placeholder="dia" />
    <input type="number" v-model="imputmes" placeholder="mes" />
    <input type="number" v-model="imputaño" placeholder="año" />
  </div>
  <div>
    <!-- Seria el componente hijo que imprime la fecha -->
    <ImprimirFecha :dia="imputdia" :mes="imputmes" :año="imputaño" />
  </div>

  <!-- Seria el componente hijo que elimina los datos de la fecha       Serian funciones para actualizar los datos de los props -->
  <Eliminar :dia="imputdia" :mes="imputmes" :año="imputaño" @delete-fecha = "changeValue"/>

</template>

<script>

// Seria para exportar los datos para ser usados por los hijos
export default {
  data() {
    return {
      imputdia: '',
      imputmes: '',
      imputaño: ''   
    }
  },
  // Seria los metodos usados para actualizar los datos de las props 
  methods:{
    changeValue(dia,mes,ano){
      this.imputdia = dia
      this.imputmes = mes
      this.imputaño = ano
    },
  }
}
</script>
<style scoped></style>
