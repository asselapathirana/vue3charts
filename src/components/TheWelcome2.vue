<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import ToolingIcon from './icons/IconTooling.vue'
import Graph2 from '../components/Graph2.vue'
</script>

<template>
 

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Graph2</template>
    <Graph2 />
  </WelcomeItem>
</template>
