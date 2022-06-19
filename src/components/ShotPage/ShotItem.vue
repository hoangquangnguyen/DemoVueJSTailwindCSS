<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
    name: "ShotItem",
    props: {
        name: String,
        company: String,
        img: String,
        like: String,
        view: String,

    },
    data() {
        return {
            ishover: false,

        }
    },
});
</script>

<template>
    <div>
        <div class="relative flex flex-col items-center" @mouseover="() => { ishover = true }"
            @mouseleave="() => { ishover = false }">
            <img :src="img" class="h-full w-full rounded-lg">
            <div class="flex flex-row items-center justify-around w-full h-1/3 px-3 absolute bottom-0 rounded-b-lg bg-gradient-to-b from-transparent to-black opacity-90 "
                :style="{ visibility: ishover ? 'visible' : 'hidden' }">
                <div class="align-baseline w-2/3 text-white">{{ name }}</div>
                <div class=" flex flex-row gap-3 items-center justify-around w-1/3 px-2">
                    <button class="bg-white p-1 rounded-md hover:bg-gray-200">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd"
                                d="M4 4a2 2 0 00-2 2v8a2 2 0 002 2h12a2 2 0 002-2V8a2 2 0 00-2-2h-5L9 4H4zm7 5a1 1 0 10-2 0v1H8a1 1 0 100 2h1v1a1 1 0 102 0v-1h1a1 1 0 100-2h-1V9z" />
                        </svg>
                    </button>
                    <button class="bg-white p-1 rounded-md hover:bg-gray-200">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd"
                                d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z"
                                clip-rule="evenodd" />
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <div class=" flex flex-row items-center justify-between">
            <div>icon</div>
            <div>{{ company }}</div>
            <div>{{ like }}</div>
            <div>{{ view }}</div>
        </div>
    </div>
</template>

<style>
</style>