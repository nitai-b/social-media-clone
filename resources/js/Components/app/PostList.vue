<script setup>
import PostItem from "@/Components/app/PostItem.vue";
import moment from "moment";

const post1 = {
    user: {
        id: 1,
        avatar: "https://randomuser.me/api/portraits/men/70.jpg",
        name: "John Smith",
    },
    body: `<p>some text for teh body lorem ipsum</p> <p>some text for teh body lorem ipsum</p><p>some text for teh body lorem ipsum</p>`,
    group: null,
    attachments: [
        {
            id: 1,
            name: "test.png",
            mime: "image/png",
            url: "https://picsum.photos/1000",
        },
        {
            id: 2,
            name: "test.png",
            mime: "image/png",
            url: "https://picsum.photos/1000",
        },
        {
            id: 3,
            name: "document.docx",
            mime: "application/document",
            url: "",
        },
    ],
    created_at: moment(new Date()).format("llll"),
};
const post2 = {
    user: {
        id: 2,
        avatar: "https://randomuser.me/api/portraits/men/70.jpg",
        name: "John Smith",
    },
    body: `<p>some more lorem ipsum</p> <p>some text for teh body lorem ipsum</p><p>some text for teh body lorem ipsum</p>`,
    group: {
        id: 1,
        name: "Laravel Developers",
    },
    created_at: moment(new Date()).format("llll"),
};
</script>

<template>
    <div class="flex-1 overflow-auto">
        <PostItem :post="post1" />
        <PostItem :post="post2" />
    </div>
</template>
