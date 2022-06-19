<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
    name: "BannerView",
    components: {

    },
    data() {
        return {
            myindex: false,
            msd: false
        }
    },
    methods: {
        mouseover() {
            this.myindex = true;
        },
        mouseleave() {
            this.myindex = false;
        },
    },
});
</script>
<template>
    <div class="max-w-max h-full  flex flex-col items-center laptop:flex-row  bg-[#FAF9FE] z-10 p-3">
        <div
            class="flex flex-col w-5/6 laptop:w-1/2 items-center text-center laptop:text-left laptop:items-start p-4 gap-2 order-2 laptop:order-1">
            <h1 class="text-3xl font-bold">Explore the world's leading design portfolips</h1>
            <span>Millions of designers and agencies around the world showcase their portfolio work on Dribbble - the
                home to the world’s best design and creative professionals</span>
            <button
                class="text-white font-semibold bg-pink-500 hover:bg-pink-400 transition duration-300 ease-out py-2 px-3 rounded-lg">Sign
                up</button>
        </div>
        <div class="w-1/2 items-end mr-5 order-1 laptop:order-2">
            <img src="@/assets/banner.png" class="laptop:h-5/6 laptop:w-5/6" />
        </div>

    </div>
</template>