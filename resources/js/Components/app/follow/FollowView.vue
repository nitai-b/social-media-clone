<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
import { ChevronUpIcon } from "@heroicons/vue/20/solid";
import FollowList from "@/Components/app/follow/FollowList.vue";
</script>

<template>
    <div class="px-3 bg-white rounded border h-full py-3 overflow-hidden">
        <div class="block lg:hidden">
            <Disclosure v-slot="{ open }">
                <DisclosureButton class="w-full">
                    <div class="flex justify-between items-center">
                        <h2 class="text-2xl font-bold">My Follows</h2>
                        <ChevronUpIcon
                            :class="open ? 'rotate-180 transform' : ''"
                            class="h-5 w-5 text-purple-500 transition-all"
                        />
                    </div>
                </DisclosureButton>
                <DisclosurePanel class="">
                    <FollowList />
                </DisclosurePanel>
            </Disclosure>
        </div>

        <div class="h-full flex-col overflow-hidden hidden lg:flex">
            <h2 class="text-2xl font-bold mb-4">My Follows</h2>
            <FollowList />
        </div>
    </div>
</template>
