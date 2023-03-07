<script setup lang="ts">
    import Navigation from "../components/header/navigation.vue"
    import Aboutme from "~~/components/about/aboutme.vue"
</script>

<template>
    <div class="flex flex-col h-full w-screen bg-gradient-to-r from-slate-800 to-pink-700 py-8 px-24">
        <Navigation></Navigation>
        <Aboutme></Aboutme>
    </div>
</template>
