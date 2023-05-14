<template>
  <main class="flex flex-col h-screen px-4 py-12 text-center">
    <slot class="flex-grow" />
    <div class="mt-auto">
      <NavMenu />
      <Footer />
    </div>
  </main>
</template>
