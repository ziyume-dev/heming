<script setup lang="ts">
const { isMobile } = useDevice()
</script>

<template>
  <MobileHome v-if="isMobile" />
  <Home v-else />
</template>
