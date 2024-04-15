<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
import { ChevronUpIcon } from "@heroicons/vue/20/solid";
import TextInput from "@/Components/TextInput.vue";
import GroupItem from "@/Components/app/group/GroupItem.vue";
import { ref } from "vue";

const searchKeyword = ref("");
</script>

<template>
    <div class="px-3 bg-white rounded border h-full py-3 overflow-hidden">
        <div class="block lg:hidden">
            <Disclosure v-slot="{ open }">
                <DisclosureButton class="w-full">
                    <div class="flex justify-between items-center">
                        <h2 class="text-2xl font-bold">My Groups</h2>
                        <ChevronUpIcon
                            :class="open ? 'rotate-180 transform' : ''"
                            class="h-5 w-5 text-purple-500 transition-all"
                        />
                    </div>
                </DisclosureButton>
                <DisclosurePanel class="">
                    <TextInput
                        v-model="searchKeyword"
                        placeholder="type to search"
                        class="w-full mt-4"
                    />
                    <div class="mt-3 h-[200px] lg:flex-1 overflow-auto">
                        <div v-if="false">
                            <div
                                class="text-gray-400 text-center justify-center p-3"
                            >
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
                </DisclosurePanel>
            </Disclosure>
        </div>

        <div class="h-full flex-col overflow-hidden hidden lg:flex">
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
    </div>
</template>
