<script setup lang="ts">
    const props = defineProps<{
        to: string,
        title: string
    }>()
</script>

<template>
    <a class="link" :href="props.to">
        {{ props.title }}
    </a>
</template>

<style scoped>
    .link {
        @apply flex flex-col grow items-center justify-center min-w-[228px] h-16 bg-red-500 text-3xl text-white p-5 rounded-lg
                hover:bg-white hover:text-red-500 hover:scale-105 transition-colors
    }
</style>
