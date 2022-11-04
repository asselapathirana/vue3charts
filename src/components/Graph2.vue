<template>
 <Chart
    :size="{ width: 500, height: 500 }"
    :data="data"
    :margin="margin"
    :direction="direction"
    :axis="axis">

    <template #layers>
      <Grid strokeDasharray="2,2" />
      <Line :dataKeys="['name', 'pl']" />
      <Line :dataKeys="['name', 'avg']" :lineStyle="{ stroke: 'red' }" type="step" />
    </template>

    <template #widgets>
      <Tooltip

      />
    </template>

</Chart>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { Chart, Grid, Line, Tooltip } from 'vue3-charts'
import { plByMonth } from '@/data'

const data = ref(plByMonth)
const direction = ref('horizontal')
const margin = ref({
  left: 0,
  top: 20,
  right: 20,
  bottom: 0
})

const axis = ref({
  primary: {
    type: 'band',
    format: (val: string) => {
      if (val === 'Feb') {
        return '😜'
      }
      return val
    }
  },
  secondary: {
    domain: ['dataMin', 'dataMax + 100'],
    type: 'linear',
    ticks: 8
  }
})

</script>

<style>
#app {
  color: #2ecc71
}
</style>