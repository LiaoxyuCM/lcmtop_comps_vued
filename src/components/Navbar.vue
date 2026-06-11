<script setup lang="ts">
    import { ref, onMounted } from "vue";
    const isUnscrolled = ref<boolean>(false);
    const isMobile = ref<boolean>(false);
    const isMenuOpen = ref<boolean>(false);

    onMounted(() => {
        window.addEventListener("resize", () => {
            isMobile.value = window.innerWidth <= 600;
        });
    })
</script>

<template>
    <nav :class="(isUnscrolled) ? 'unscrolled' : ''">
        <a href="/">LiaoxyuCM</a>
        <div class="pe" v-if="isMobile">
            <svg width="24" height="24" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" @click="() => {isMenuOpen = !isMenuOpen}">
                <path
                    fill="none"
                    strokeLinecap="round"
                    strokeMiterlimit="10"
                    strokeWidth="1.5"
                    stroke="currentColor"
                    d="M3.75 7.5h16.5M3.75 12h16.5M3.75 16.5h16.5"
                />
            </svg>
        </div>
        <div class="pc" v-else>
            <a href="https://github.com/LiaoxyuCM" target="_blank">
               GitHub
            </a>
            <a href="https://llcm.top/friendlylinks" target="_blank">
               友链
            </a>
        </div>
        <div v-if="isMobile" :class="`mobile-menu ${isMenuOpen ? 'open' : ''}`">
            <button
                class="close-btn ignore-button-default-style"
                @click="() => {isMenuOpen = !isMenuOpen}">
                ✕
            </button>
            <a href="https://github.com/LiaoxyuCM" target="_blank">
               GitHub
            </a>
            <a href="https://llcm.top/friendlylinks" target="_blank">
               友链
            </a>
        </div>
    </nav>
</template>