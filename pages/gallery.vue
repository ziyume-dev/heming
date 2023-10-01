<script setup lang="ts">
const info = ref([
  {
    title: 'DiyFile',
    desc: '一款好看的在线文件列表程序，由 Spring Boot 3 和 Vue 驱动。',
    href: 'https://github.com/besscroft/diyfile',
    target_title: 'GitHub',
  },
  {
    title: 'HeMing Fast',
    desc: '基于 SpringBoot3 + Nuxt 3 + Vuetify 3 的脚手架！',
    href: 'https://github.com/besscroft/heming-fast',
    target_title: 'GitHub',
  },
  {
    title: '嗯学英语',
    desc: '嗯学英语，学英语，就嗯学！',
    href: 'https://github.com/besscroft/enstudy',
    target_title: 'GitHub',
  },
  {
    title: 'duduke',
    desc: '蹦蹦火花，是可莉的核武器啦！',
    href: '#',
    target_title: 'N/A',
  },
  {
    title: 'duduke-clip',
    desc: '嘟嘟可 CLIP 模型炼丹系统！',
    href: '#',
    target_title: 'N/A',
  },
])

definePageMeta({
  layout: 'default',
})
</script>

<template>
  <div grid grid-cols-1 gap-3 md:grid-cols-3 md:gap-8 mxa md:mt-8 md:px-20>
    <div :key="item" v-for="item in info" flex flex-col items-center h-48 rounded-md border-green-400 border-4 px-4>
      <div h-12 flex items-center><p text-xl>{{ item.title }}</p></div>
      <div h-24 p-2><p>{{ item.desc }}</p></div>
      <a h-12 p-2 icon-btn rel="noreferrer" :href="item.href" target="_blank" :title="item.target_title">
        <div animate-bounce scale-150 i-carbon-send-alt />
      </a>
    </div>
  </div>
</template>

<style scoped>

</style>
