<template>
    <!-- Container -->
    <div class="p-4 bg-pink-500 flex flex-col gap-4 w-full">
        <!-- Title -->
        <h2 class="font-eiko bg-amber-500 text-7xl">{{ title }}</h2>

        <!-- Left -->
        <div class="bg-green-500 flex fles-row gap-4">
            <!-- Slider -->
            <div class="bg-orange-500 flex flex-col gap-4 w-3/5">
                <!-- Image -->
                <img
                    class="h-[677px] w-full object-cover"
                    :src="image"
                    :alt="title"
                />

                <!-- Slider Indicator -->
                <div class="bg-yellow-500 flex flex-row gap-2">
                    <div class="h-2 w-16 bg-blue-500 hover:bg-gray-800" />
                    <div class="h-2 w-16 bg-blue-500 hover:bg-gray-800" />
                    <div class="h-2 w-16 bg-blue-500 hover:bg-gray-800" />
                    <div class="h-2 w-16 bg-blue-500 hover:bg-gray-800" />
                </div>
            </div>

            <!-- Content -->
            <div class="bg-purple-500 flex flex-col gap-4 w-2/5">
                <!-- Description -->
                <p class="font-neue-montreal text-2xl leading-[1.5]">
                    {{ description }}
                </p>

                <!-- Link -->
                <NuxtLink
                    to="https://www.google.com"
                    class="font-neue-montreal text-2xl font-bold text-black hover:text-gray-500 tracking-wide capitalize"
                    >Read More <span class="ml-1">→</span></NuxtLink
                >

                <!-- Divider -->
                <div class="h-[1px] width-full bg-gray-200 my-2" />

                <!-- Tags -->
                <div class="bg-neutral-500 flex flex-row gap-2">
                    <Tag text="Tag 1" />
                    <Tag text="Tag 2" />
                    <Tag text="Tag 3" />
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
defineOptions({ name: "ProjectCard" });

const { title, description } = defineProps({
    title: {
        type: String,
        required: true,
    },
    description: {
        type: String,
        required: false,
        default: "",
    },
    image: {
        type: String,
        required: true,
    },
});
</script>
