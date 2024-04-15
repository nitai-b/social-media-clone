<script setup>
import TextInput from "@/Components/TextInput.vue";
import GroupItem from "@/Components/app/group/GroupItem.vue";
import { ref } from "vue";

const searchKeyword = ref("");
</script>

<template>
    <div
        class="px-3 bg-white rounded border py-3 h-[400px] lg:h-full overflow-hidden flex flex-col"
    >
        <h2 class="text-2xl font-bold mb-4">My Groups</h2>
        <TextInput
            v-model="searchKeyword"
            placeholder="type to search"
            class="w-full"
        />
        <div class="mt-3 flex-1 overflow-auto">
            <div v-if="false">
                <div class="text-gray-400 text-center justify-center p-3">
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
    </div>
</template>
