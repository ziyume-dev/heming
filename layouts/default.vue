<template>
  <main class="flex flex-col h-screen px-4 py-12 text-center light:bg-gradient-to-r light:from-green-400 light:to-blue-500">
    <slot class="flex-grow" />
    <div class="mt-auto">
      <NavMenu />
      <Footer />
    </div>
  </main>
</template>
