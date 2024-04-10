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
            <GroupList />
            <GroupItem
                image="https://picsum.photos/100"
                title="Laravel Developers"
                description="laravel developers lorem ipsum"
            />
        </div>
        <div class="col-span-6">Posts</div>
        <div class="col-span-3">Followers</div>
    </div>
</template>
