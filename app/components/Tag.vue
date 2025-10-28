<template>
    <div
        class="font-neue-montreal bg-orange-500 px-4 py-2 inline-block rounded-full font-normal text-black hover:text-white hover:bg-orange-800 text-base capitalize"
    >
        {{ text }}
    </div>
</template>

<script setup>
defineOptions({ name: "Tag" });

const { text } = defineProps({
    text: {
        type: String,
        required: true,
    },
});
</script>
