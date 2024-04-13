<script setup>
import { Head, Link } from "@inertiajs/vue3";
import GroupList from "@/Components/app/GroupList.vue";
import FollowList from "@/Components/app/FollowList.vue";
import PostList from "@/Components/app/PostList.vue";
import CreatePost from "@/Components/app/CreatePost.vue";
defineProps();
</script>

<template>
    <Head title="Social Media Website" />
    <div class="grid grid-cols-12 gap-3">
        <div class="col-span-3 py-6">
            <GroupList />
        </div>
        <div class="col-span-6">
            <CreatePost />
            <PostList />
        </div>
        <div class="col-span-3 py-6">
            <FollowList />
        </div>
    </div>
</template>
