<script setup>
import TextInput from "@/Components/TextInput.vue";
import FollowItem from "@/Components/app/follow/FollowItem.vue";
import { ref } from "vue";

const searchKeyword = ref("");
</script>
<template>
    <TextInput
        v-model="searchKeyword"
        placeholder="type to search"
        class="w-full mt-4"
    />
    <div class="mt-3 h-[200px] lg:flex-1 overflow-auto">
        <div v-if="false">
            <div class="text-gray-400 text-center justify-center p-3">
                You have not joined any groups
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
            <FollowItem
                image="https://picsum.photos/100"
                title="Laravel Developers"
            />
            <FollowItem
                image="https://picsum.photos/100"
                title="Vue Developers"
            />
            <FollowItem
                image="https://picsum.photos/100"
                title="Laravel Developers"
            />
            <FollowItem
                image="https://picsum.photos/100"
                title="Vue Developers"
            />
            <FollowItem
                image="https://picsum.photos/100"
                title="Laravel Developers"
            />
            <FollowItem
                image="https://picsum.photos/100"
                title="Vue Developers"
            />
            <FollowItem
                image="https://picsum.photos/100"
                title="Laravel Developers"
            />
            <FollowItem
                image="https://picsum.photos/100"
                title="Vue Developers"
            />
            <FollowItem
                image="https://picsum.photos/100"
                title="Laravel Developers"
            />
            <FollowItem
                image="https://picsum.photos/100"
                title="Vue Developers"
            />
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
</template>
