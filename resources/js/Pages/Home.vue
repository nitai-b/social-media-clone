<script setup>
import { Head, Link } from "@inertiajs/vue3";
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import GroupList from "@/Components/app/group/GroupList.vue";
import FollowList from "@/Components/app/follow/FollowList.vue";
import PostList from "@/Components/app/post/PostList.vue";
import CreatePost from "@/Components/app/post/CreatePost.vue";
defineProps();
</script>

<template>
    <Head title="Social Media Website" />
    <AuthenticatedLayout>
        <div class="grid lg:grid-cols-12 gap-3 p-4 h-full">
            <div class="lg:col-span-3 lg:order-1 h-full overflow-hidden">
                <GroupList />
            </div>
            <div class="lg:col-span-3 lg:order-3 h-full overflow-hidden">
                <FollowList />
            </div>
            <div
                class="lg:col-span-6 lg:order-2 h-full overflow-hidden flex flex-col"
            >
                <CreatePost />
                <PostList class="flex-1" />
            </div>
        </div>
    </AuthenticatedLayout>
</template>
