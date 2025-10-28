<template>
    <div>
        <h1 class="font-eiko font-medium text-4xl">Home Page</h1>
        <Link to="/about">About</Link>
        <NuxtLink
            class="font-neue-montreal font-bold text-black hover:text-gray-500 text-2xl font-extrabold capitalize"
            to="/about"
            >About <span class="ml-2">→</span></NuxtLink
        >
        <Tag text="Hello" />
    </div>
</template>
