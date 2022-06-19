<script lang="ts">
import { defineComponent } from "vue";
import { hexToCSSFilter } from 'hex-to-css-filter';


export default defineComponent(
    {
        name: "NavBarLiItem",
        components: {
        },
        props: {
            title: String,
            desc: String,
            color: String
        },
        data() {
            return {
                mycolor: 'filter:' + hexToCSSFilter(this.color != null ? this.color : "#f8f8f8").filter,
            }
        },
        methods: {
            geturl() {
                return "@assets/heart-icon.png";
            }
        }
    }
);
</script>
<template>
    <li class=" flex flex-row items-center justify-start gap-3">
        <div class="p-2 bg-slate-50 hover:bg-purple-100 rounded-lg ">
            <img src="@/assets/explore-icon.svg" />
        </div>

        <a href="">
            <p>{{ title }}</p>
            <p class="text-xs font-light">{{ desc }}</p>
        </a>
    </li>
</template>