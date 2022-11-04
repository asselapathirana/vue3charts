<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import ToolingIcon from './icons/IconTooling.vue'
import Graph1 from '../components/Graph1.vue'
</script>

<template>
 

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Graph</template>
    <Graph1 />
  </WelcomeItem>
</template>
