<script setup>
defineProps({
    image: String,
    title: String,
    description: String,
});
</script>

<template>
    <div class="mb-3 cursor-pointer hover:bg-gray-100 rounded-e">
        <div class="flex items-center gap-3 py-2 px-3">
            <img :src="image" class="rounded-full w-[32px]" />
            <div>
                <h3 class="font-black text-lg">{{ title }}</h3>
                <div class="text-xs text-gray-500">
                    {{ description }}
                </div>
            </div>
        </div>
    </div>
</template>
