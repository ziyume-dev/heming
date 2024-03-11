<script setup lang="ts">
import { breakpointsTailwind, useBreakpoints } from '@vueuse/core'

const breakpoints = useBreakpoints(breakpointsTailwind)
const mdAndLarger = breakpoints.greaterOrEqual('md')
</script>

<template>
  <nav class="py-2.5">
    <div class="flex flex-wrap items-center justify-between max-w-screen-xl px-4 mx-auto">
      <RouterLink to="/">
        <h1 class="font-serif text-2xl">
          <ruby>鹤<rp>(</rp><rt>He</rt><rp>)</rp></ruby>
          <ruby>鸣<rp>(</rp><rt>Ming</rt><rp>)</rp></ruby>
          <span class="justify-center items-center inline px-2 text-3xl border-4 border-green-400" data-text="工作室">工作室</span>
        </h1>
      </RouterLink>
      <ul v-if="mdAndLarger" flex space-x-8>
        <li>
          <RouterLink border-l-4 border-green-400 icon-btn px-2 font-serif to="/gallery" title="gallery">
            作品
          </RouterLink>
        </li>
        <li>
          <RouterLink border-l-4 border-green-400 icon-btn px-2 font-serif to="/business" title="business">
            商务合作
          </RouterLink>
        </li>
        <li>
          <RouterLink border-l-4 border-green-400 icon-btn px-2 font-serif to="/about" title="about">
            关于
          </RouterLink>
        </li>
      </ul>
      <div flex items-center space-x-4>
        <DarkToggle />
        <a v-if="mdAndLarger" icon-btn mx-2 rel="noreferrer" href="https://github.com/besscroft" target="_blank" title="GitHub">
          <div i-carbon-logo-github />
        </a>
        <div v-if="!mdAndLarger">
          <MobileMenu />
        </div>
      </div>
    </div>
  </nav>
</template>
