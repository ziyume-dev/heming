<script setup lang="ts">
import { breakpointsTailwind, useBreakpoints } from '@vueuse/core'

const breakpoints = useBreakpoints(breakpointsTailwind)
const mdAndLarger = breakpoints.greaterOrEqual('md')
const { t } = useI18n()
</script>

<template>
  <button v-if="mdAndLarger" icon-btn :title="t('button.toggle_dark')" @click="toggleDark()">
    <div i="carbon-sun dark:carbon-moon" />
  </button>
</template>

<style scoped>

</style>
