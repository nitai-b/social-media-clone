<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
const props = defineProps({
    post: Object,
});
</script>

<template>
    <div class="bg-white border rounded p-4">
        <div class="flex items-center gap-2 mb-3">
            <a href="javascript:void(0)">
                <img class="w-[32px] rounded-full" :src="post.user.avatar" />
            </a>
            <div>
                <a href="javascript:void(0)">
                    <h4 class="font-bold">{{ post.user.name }}</h4>
                </a>
                <small class="text-gray-400">{{ post.created_at }}</small>
            </div>
        </div>
        <div>
            <Disclosure v-slot="{ open }">
                <div v-if="!open" v-html="post.body.substring(0, 50)" />
                <DisclosurePanel class="">
                    <div v-html="post.body" />
                </DisclosurePanel>
                <div class="flex justify-end">
                    <DisclosureButton class="text-blue-500">
                        {{ open ? "Read less" : "Read more" }}
                    </DisclosureButton>
                </div>
            </Disclosure>
        </div>
    </div>
</template>
