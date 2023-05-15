<script setup lang="ts">
definePageMeta({
    layout: 'default',
})
</script>

<template>
    <div pt-4>
        <NuxtLink to="/">
            <h1 class="font-serif text-6xl">
                <ruby>鹤<rp>(</rp><rt>He</rt><rp>)</rp></ruby>
                <ruby>鸣<rp>(</rp><rt>Ming</rt><rp>)</rp></ruby>
                <span class="justify-center items-center inline px-2 text-3xl border-4 light:border-pink-100" data-text="工作室">工作室</span>
            </h1>
        </NuxtLink>

        <div class="py-16 max-w-xl mxa">
            <p class="text-2xl text-center font-semibold">鹤鸣</p>

            <p class="text-left mx-2 mt-4">
                鹤鸣于九皋，声闻于野。鱼潜在渊，或在于渚。乐彼之园，爰有树檀，其下维萚。他山之石，可以为错。
            </p>

            <p class="text-left mx-2 mt-2">
                鹤鸣于九皋，声闻于天。鱼在于渚，或潜在渊。乐彼之园，爰有树檀，其下维谷。他山之石，可以攻玉。
            </p>

            <p class="text-right mt-2">——《诗经‧小雅-鸿雁之什‧鹤鸣》</p>
        </div>

        <p>装修中...</p>
    </div>
</template>
