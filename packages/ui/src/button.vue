<script lang="ts" setup>
import { computed } from 'vue';

const props = defineProps<{
    type: 'primary' | 'secondary' | 'error';
}>();
const bgColor = computed(() => {
    return {
        primary: 'blue',
        secondary: 'gray',
        error: 'red',
    }[props.type];
});
</script>

<template>
    <button
        :style="{
            backgroundColor: bgColor,
        }"
    ></button>
</template>
