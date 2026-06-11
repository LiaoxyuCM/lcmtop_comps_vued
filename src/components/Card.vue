<script setup lang="ts">    
    defineProps({
        title: {
            type: String,
            required: true,
        },
        content: {
            type: String,
            required: true,
        },
        link: {
            type: String,
            required: true,
        },
        targetblank: {
            type: Boolean,
            required: false,
            default: false,
        },
        visible: {
            type: Boolean,
            required: false,
            default: true,
        },
    })
</script>

<template>
    <a :href="link" :style="`display: ${visible ? 'block' : 'none'}`" :target="targetblank ? '_blank' : '_self'">
        <div class="card">
            <h3>{{ title }}</h3>
            <p class="description">{{ content }}</p>
        </div>
    </a>
</template>