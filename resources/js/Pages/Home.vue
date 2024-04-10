<script setup>
import { Head, Link } from "@inertiajs/vue3";
import GroupList from "@/Components/app/GroupList.vue";
import GroupItem from "@/Components/app/GroupItem.vue";
defineProps();
</script>

<template>
    <Head title="Social Media Website" />
    <div class="grid grid-cols-12 gap-3">
        <div class="col-span-3 py-6 px-3">
            <h2 class="text-2xl font-bold px-3">My Groups</h2>
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
        </div>
        <div class="col-span-6">Posts</div>
        <div class="col-span-3">Followers</div>
    </div>
</template>
