<script setup lang="ts">
import { appName } from '~/constants'

const { isMobile } = useDevice()

useHead({
  title: appName,
})
</script>

<template>
  <VitePwaManifest />
  <NuxtLayout :name="isMobile ? 'mobile' : 'default'">
    <NuxtPage />
  </NuxtLayout>
</template>

<style>
html, body , #__nuxt{
  height: 100vh;
  margin: 0;
  padding: 0;
}

html.dark {
  background: #222;
  color: white;
}
</style>
