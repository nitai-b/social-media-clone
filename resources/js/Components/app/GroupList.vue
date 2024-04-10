<script setup>
import TextInput from "@/Components/TextInput.vue";
import GroupItem from "@/Components/app/GroupItem.vue";
import { ref } from "vue";

const searchKeyword = ref("");
</script>

<template>
    <h2 class="text-2xl font-bold px-3">My Groups</h2>
    <TextInput v-model="searchKeyword" placeholder="type to search" />
    <div class="py-8">
        <div v-if="false">
            <div class="text-gray-400 flex text-center justify-center">
                You have not joined any groups
            </div>
        </div>
        <div v-else="">
            <GroupItem
                image="https://picsum.photos/100"
                title="Laravel Developers"
                description="laravel developers lorem ipsum"
            />
            <GroupItem
                image="https://picsum.photos/100"
                title="Vue Developers"
                description="laravel developers lorem ipsum"
            />
        </div>
    </div>
</template>
