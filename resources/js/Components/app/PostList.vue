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
    created_at: moment(new Date()).format("llll"),
};
</script>

<template>
    <div>
        <PostItem :post="post1" />
    </div>
</template>
