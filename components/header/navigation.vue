<script setup>
    import nav from "../../static/nav.json"

    const appConfig = useAppConfig()
    const navItems = nav.items
</script>

<template>
    <section class="flex justify-between">
        <div class="flex gap-x-2">
            <span class="animation-4">
                <span class="text-3xl text-white">{{ appConfig.title.split(' ')[0] }}</span>
                <span class="text-3xl text-red-500 ml-3">{{ appConfig.title.split(' ')[1] }}</span>
            </span>
        </div>
        <div class="flex gap-x-6">
            <template v-for="item in navItems">
                <span class="text-xl text-white hover:text-slate-800 transition-colors">
                    <NuxtLink :to="item.link">
                        {{ item.title }}
                    </NuxtLink>
                </span>
            </template>
        </div>
    </section>
</template>
