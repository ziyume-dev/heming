<script setup lang="ts">
const color = useColorMode()

useHead({
    meta: [{
        id: 'theme-color',
        name: 'theme-color',
        content: () => color.value === 'dark' ? '#222222' : '#ffffff',
    }],
})

function toggleDark() {
    color.preference = color.value === 'dark' ? 'light' : 'dark'
}
</script>

<template>
    <nav text-xl my-2>
        <NuxtLink class="icon-btn mx-2" to="/" title="Home">
            <div i-carbon-home />
        </NuxtLink>

        <button class="icon-btn mx-2 !outline-none" @click="toggleDark()" title="toggleDark">
            <div class="i-carbon-sun dark:i-carbon-moon" />
        </button>

        <NuxtLink class="icon-btn mx-2" to="/about" title="about">
            <div class="i-carbon-warning dark:i-carbon-warning-filled" />
        </NuxtLink>

        <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/besscroft" target="_blank" title="GitHub">
            <div i-carbon-logo-github />
        </a>
    </nav>
</template>