<script setup>
defineProps({
  dia: {
    type: Number,
    required: true
  },
  mes: {
    type: Number,
    required: true
  },
  año: {
    type: Number,
    required: true
  }
})
</script>

<template>
  <div>
    <!-- Se imprime la fecha -->
    <button @click="esactivo">enviar</button>
    <p>{{ diaD }}/{{ mesM }}/{{ añoA }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      diaD: 'DD',
      mesM: 'MM',
      añoA: 'AAAA',
      isActive: false
    }
  },
  methods: {
    esactivo() {
      this.isActive = true; // Bandera para saber si el boton fue presionado
      this.diaD = this.$props.dia;
      this.mesM = this.$props.mes;
      this.añoA = this.$props.año;
    }
  },
  watch:{
    dia: function(newValue, valueBefore){
      if (this.isActive === true){
        this.diaD = newValue
      }
    },
    mes:function(newValue,valueBefore){
      if(this.isActive === true){
        this.mesM = newValue
      }
    },
    año: function(newValue,valueBefore){
      if (this.isActive === true){
        this.añoA = newValue
      }
    }
  }
}
</script>

<style scoped></style>
