<script setup lang="ts">
import { DrawerClose, DrawerContent, DrawerOverlay, DrawerPortal, DrawerRoot, DrawerTrigger } from 'vaul-vue'

const router = useRouter()
const route = useRoute()

const routerList = ref([
  {
    index: 1,
    title: '作品',
    link: '/gallery',
  },
  {
    index: 2,
    title: '商务合作',
    link: '/business',
  },
  {
    index: 3,
    title: '关于',
    link: '/about',
  },
])
</script>

<template>
  <DrawerRoot should-scale-background>
    <DrawerTrigger rounded-full px-4 py-2.5 shadow-sm ring-1 ring-inset ring-gray-300 cursor-pointer>
      <div i-carbon-app />
    </DrawerTrigger>
    <DrawerPortal>
      <DrawerOverlay fixed dark:bg-slate-800 inset-0 class="bg-black/40" />
      <DrawerContent
        bg-gray-100 dark:bg-slate-900 flex flex-col h-full mt-24 fixed bottom-0 left-0 right-0
        class="rounded-t-[10px]  max-h-[96%]"
      >
        <div
          flex-1 p-4 bg-white dark:bg-slate-900
          class="rounded-t-[10px]"
        >
          <div mx-auto w-12 h-1.5 flex-shrink-0 rounded-full bg-gray-300 mb-8 />
          <div>
            <div flex flex-col>
              <DrawerClose
                v-for="item in routerList"
                :key="item.index"
                @click="router.push(item.link)"
                flex flex-row items-center rounded
                block px-5 py-2 focus-blue w-full
                transition-colors duration-200 transform text-gray-700 dark:text-gray-200
                hover="bg-gray-100 dark:(bg-gray-700 text-white)"
                :class="route.path === item.link ? 'bg-gray-100 dark:(bg-gray-700 text-white)' : ''"
              >
                {{ item.title }}
              </DrawerClose>
            </div>
            <div border="neutral-300 dark:neutral-700 t-1" mx-3 my-2 />
            <div flex flex-col>
              <DrawerClose
                flex flex-row items-center rounded
                block px-5 py-2 focus-blue w-full
                transition-colors duration-200 transform text-gray-700 dark:text-gray-200
                hover="bg-gray-100 dark:(bg-gray-700 text-white)"
              >
                <a rel="noreferrer" href="https://github.com/besscroft" target="_blank" title="GitHub">
                  GitHub
                </a>
              </DrawerClose>
            </div>
          </div>
        </div>
      </DrawerContent>
    </DrawerPortal>
  </DrawerRoot>
</template>
