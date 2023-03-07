<script setup>
    import Navigation from "../components/header/navigation.vue"
    import Link from "../components/link/link.vue"
    import links from "../static/links.json"
    import Popper from "vue3-popper"

    const linkItems = ref(links.items)
</script>

<template>
    <div class="flex flex-col h-screen w-screen bg-gradient-to-r from-slate-800 to-pink-700 py-8 px-24">
        <Navigation></Navigation>
        <div class="flex flex-col justify-center items-center h-full animation-1">
            <section class="flex flex-wrap max-w-4xl gap-4">
                <template v-for="link in linkItems">
                    <Popper
                        class="flex grow"
                        :show="link.popper.show"
                        :content="link.popper.content"
                    >
                        <Link
                            @mouseenter="link.popper.show = true"
                            @mouseleave="link.popper.show = false"
                            :to="link.link"
                            :title="link.title"
                        >
                        </Link>
                    </Popper>
                </template>
            </section>
        </div>
    </div>
</template>
