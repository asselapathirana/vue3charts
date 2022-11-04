<template>
  <Chart
    :size="{ width: 800, height: 800 }"
    :data="data"
    :margin="margin"
    :direction="direction">
    <template #layers>
      <Grid strokeDasharray="2,2" />
      <Line :dataKeys="['name', 'pl']" />
    </template>

  </Chart>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { Chart, Grid, Line } from 'vue3-charts'
import { plByMonth } from '@/data'
const data = ref(plByMonth)
const direction = ref('horizontal')
const margin = ref({
      left: 0,
      top: 20,
      right: 20,
      bottom: 0
})

</script>

<style>
#app {
  color: #2ecc71
}
</style>