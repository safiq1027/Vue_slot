<script setup>
import{ ref } from 'vue'
</script>
<template>
    <p>
        <slot name="header"></slot>
    </p>
    <p class="my-10">
        <slot name="default"> </slot>
    </p>
    <p>
        <slot name="footer"></slot>
    </p>
</template>
<style scoped></style>