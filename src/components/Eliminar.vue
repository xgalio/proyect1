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
        <button @click="changeValue">Eliminar</button>
    </div>
</template>

<script>
export default {
  methods: {
    changeValue(){
        this.$emit('delete-fecha', 'DD', 'MM', 'AAAA') // Este evento sirve para cambiar los valores de los props del padre
    }
  }
}
</script>