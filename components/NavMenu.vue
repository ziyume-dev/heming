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

function mobileMenuToggle() {
  const mobileMenu = document.getElementById('mobile-menu')
  mobileMenu.classList.toggle('hidden')
}
</script>

<template>
  <nav class="py-2.5">
    <div class="flex flex-wrap items-center justify-between max-w-screen-xl px-4 mx-auto">
      <NuxtLink to="/">
        <h1 class="font-serif text-2xl">
          <ruby>鹤<rp>(</rp><rt>He</rt><rp>)</rp></ruby>
          <ruby>鸣<rp>(</rp><rt>Ming</rt><rp>)</rp></ruby>
          <span class="justify-center items-center inline px-2 text-3xl border-4 light:border-pink-100" data-text="工作室">工作室</span>
        </h1>
      </NuxtLink>
      <div class="flex items-center md:order-2">
        <button class="icon-btn mx-2 !outline-none" @click="toggleDark()" title="toggleDark">
          <div class="i-carbon-sun dark:i-carbon-moon" />
        </button>
        <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/besscroft" target="_blank" title="GitHub">
          <div i-carbon-logo-github />
        </a>
        <button @click="mobileMenuToggle" type="button" class="inline-flex items-center p-2 ml-1 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
          <svg class="hidden w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
        </button>
      </div>
      <div class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1" id="mobile-menu">
        <ul flex flex-col mt-4 font-medium md:flex-row md:space-x-8 md:mt-0 space-y-2 sm:space-y-0>
          <li>
            <NuxtLink border-l-4 light:border-pink-100 icon-btn px-2 font-serif to="/gallery" title="gallery">
              作品
            </NuxtLink>
          </li>
          <li>
            <NuxtLink border-l-4 light:border-pink-100 icon-btn px-2 font-serif to="/business" title="business">
              商务合作
            </NuxtLink>
          </li>
          <li>
            <NuxtLink border-l-4 light:border-pink-100 icon-btn px-2 font-serif to="/about" title="about">
              关于
            </NuxtLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
