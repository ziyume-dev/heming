<script setup lang="ts">
const { t, availableLocales, locale } = useI18n()

function toggleLocales() {
  // change to some real logic
  const locales = availableLocales
  locale.value = locales[(locales.indexOf(locale.value) + 1) % locales.length]
}
</script>

<template>
  <nav text-xl my-4>
    <RouterLink class="icon-btn mx-2" to="/" :title="t('button.home')">
      <div i-ri-home-2-line />
    </RouterLink>

    <button class="icon-btn mx-2 !outline-none" :title="t('button.toggle_dark')" @click="toggleDark()">
      <div i="ri-sun-line dark:ri-moon-line" />
    </button>

    <RouterLink class="icon-btn mx-2" to="/about" :title="t('button.about')">
      <div i-ri-information-line />
    </RouterLink>

    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/besscroft" target="_blank" title="GitHub">
      <div i-ri-github-line />
    </a>
  </nav>
</template>
