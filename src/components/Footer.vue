<script setup lang="ts">
    import { ref } from 'vue';

    const footer_copyright_content = ref<string>(`© LiaoxyuCM Lclimir × LcmTech 2024-${new Date().getFullYear()}`);
</script>

<template>
    <footer>
        <p @click="footer_copyright_content = 'Hello, QiChong & QiJun Chlorine!'"
        >{{ footer_copyright_content }}</p>
    </footer>
</template>