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
    <p>{{ dia }}/{{ mes }}/{{ año }}</p>
  </div>
</template>

<style scoped></style>
