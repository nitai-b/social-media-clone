<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
const props = defineProps({
    post: Object,
});

function isImage(attachment) {
    const mime = attachment.mime.split("/");
    return mime[0].toLowerCase() === "image";
}
</script>

<template>
    <div class="bg-white border rounded p-4 my-2">
        <div class="flex gap-2 mb-3">
            <a href="javascript:void(0)">
                <img
                    class="w-[32px] rounded-full border-2 transition-all hover:border-blue-400"
                    :src="post.user.avatar"
                />
            </a>
            <div>
                <h4 class="font-bold">
                    <a class="hover:underline" href="javascript:void(0)">
                        {{ post.user.name }}
                    </a>
                    <a
                        class="hover:underline"
                        v-if="post.group !== null"
                        href="javascript:void(0)"
                    >
                        | {{ post.group.name }}
                    </a>
                </h4>

                <small class="text-gray-400">{{ post.created_at }}</small>
            </div>
        </div>
        <div>
            <Disclosure v-slot="{ open }">
                <div v-if="!open" v-html="post.body.substring(0, 50) + '...'" />
                <DisclosurePanel class="">
                    <div v-html="post.body" />
                </DisclosurePanel>
                <div class="flex justify-end mb-3">
                    <DisclosureButton class="text-blue-500 hover:underline">
                        {{ open ? "Read less" : "Read more" }}
                    </DisclosureButton>
                </div>
            </Disclosure>
        </div>
        <div
            v-if="post.attachments !== null"
            class="grid grid-cols-2 lg:grid-cols-3 gap-3"
        >
            <div v-for="attachment of post.attachments">
                <div
                    class="aspect-square bg-blue-50 flex flex-col justify-center items-center relative"
                >
                    <button
                        class="absolute w-8 h-8 bg-gray-700 right-2 top-2 cursor-pointer rounded flex items-center justify-center hover:bg-gray-800 text-white"
                    >
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke-width="1.5"
                            stroke="white"
                            class="w-4 h-4"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                d="M3 16.5v2.25A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75V16.5M16.5 12 12 16.5m0 0L7.5 12m4.5 4.5V3"
                            />
                        </svg>
                    </button>
                    <img
                        v-if="isImage(attachment)"
                        :src="attachment.url"
                        class="object-cover aspect-square"
                    />
                    <div
                        v-else
                        class="flex flex-col items-center justify-center"
                    >
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke-width="1.5"
                            stroke="currentColor"
                            class="w-16 h-16"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                d="M19.5 14.25v-2.625a3.375 3.375 0 0 0-3.375-3.375h-1.5A1.125 1.125 0 0 1 13.5 7.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H8.25m2.25 0H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 0 0-9-9Z"
                            />
                        </svg>
                        {{ attachment.name }}
                    </div>
                </div>
            </div>
        </div>
        <div><button>like</button></div>
        <div><button>comment</button></div>
    </div>
</template>
