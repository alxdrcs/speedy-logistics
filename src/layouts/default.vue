<script setup lang="ts">
import JHeader from './JHeader.vue';
import JFooter from './JFooter.vue';
</script>

<template>
  <JHeader />
  <slot />
  <JFooter />
</template>