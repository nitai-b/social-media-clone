<script setup>
import TextInput from "@/Components/TextInput.vue";
import FollowItem from "@/Components/app/FollowItem.vue";
import { ref } from "vue";

const searchKeyword = ref("");
</script>

<template>
    <div class="px-3">
        <h2 class="text-2xl font-bold mb-4">My Follows</h2>
        <TextInput v-model="searchKeyword" placeholder="type to search" />
        <div class="py-8">
            <div v-if="false">
                <div class="text-gray-400 flex text-center justify-center">
                    You aren't following anyone yet
                </div>
            </div>
            <div v-else="">
                <FollowItem
                    image="https://picsum.photos/100"
                    title="Laravel Developers"
                />
                <FollowItem
                    image="https://picsum.photos/100"
                    title="Vue Developers"
                />
            </div>
        </div>
    </div>
</template>
