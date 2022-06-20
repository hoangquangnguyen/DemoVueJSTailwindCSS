<script lang="ts">
import { defineComponent } from "vue";
import NavBarLiItem from "./NavBarLiItem.vue";
import NavBarLiItem2 from "./NavBarLiItem2.vue";
export default defineComponent({
    name: "NavBar",
    components: {
        NavBarLiItem,
        NavBarLiItem2
    },
    data() {
        return {
            isTab1: false,
            isTab2: false,
            isTab3: false,
            isTab4: false,
            isTab5: false,
            isTab6: false,
        }
    },
    methods: {
        mouseover() {
            this.isTab1 = true;
        },
        mouseleave() {
            this.isTab1 = false;
        },
    },
});
</script>

<template>
    <div class="flex flex-row items-center justify-between text-gray-600 h-14 px-8">
        <div class="laptop:hidden">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
        </div>

        <div>
            <a href="https://dribbble.com/">
                <img src="@/assets/logo.svg" class="hover:contrast-0" />
            </a>

        </div>

        <div class="hidden laptop:block h-full">
            <ul class="flex flex-row gap-4 items-center justify-center h-full text-sm font-semibold ">
                <!-- DropMenu1  -->
                <li @mouseover="() => { isTab1 = true }" @mouseleave="() => { isTab1 = false }" class="z-20 py-3">
                    <a>Inspiration</a>
                    <div :style="{ visibility: isTab1 ? 'visible' : 'hidden' }"
                        class="fixed p-6 rounded-xl shadow-[0px_2px_30px_5px_rgba(0,0,0,0.1)] transform translate-y-2 -translate-x-8 bg-white">
                        <ul class=" flex flex-col items-start gap-5">
                            <NavBarLiItem2 imgurl="@/assets/search-icon.svg" title="Explore Design Work"
                                desc="Trending designs to inspire you" />
                            <NavBarLiItem2 imgurl="@/assets/search-icon.svg" title="New & Noteworthy"
                                desc="Up-and-coming designers" />
                            <NavBarLiItem2 imgurl="@/assets/search-icon.svg" title="Playoff"
                                desc="Work designers are riffing on" />
                            <NavBarLiItem2 imgurl="@/assets/search-icon.svg" title="Blog"
                                desc="Interviews, tutorials, and more" />
                            <NavBarLiItem2 imgurl="@/assets/search-icon.svg" title="Weekly Warm-up"
                                desc="Prompt to flex your design skills" />
                        </ul>
                    </div>
                </li>
                <!-- DropMenu2  -->
                <li @mouseover="() => { isTab2 = true }" @mouseleave="() => { isTab2 = false }" class="z-20 py-3">
                    <a>Find Work</a>
                    <div :style="{ visibility: isTab2 ? 'visible' : 'hidden' }"
                        class="fixed p-6 rounded-xl shadow-[0px_2px_30px_5px_rgba(0,0,0,0.1)] transform translate-y-2 -translate-x-8 bg-white">
                        <ul class=" flex flex-col items-start gap-5">
                            <NavBarLiItem title="Job Board" desc="Find your dream design job" />
                            <NavBarLiItem title="Freelance Projects" desc="An exclusive list for contract work" />
                            <hr size="1px" width="90%" />
                            <NavBarLiItem title="Want freelance design projects?"
                                desc="Get new leads in your inbox every day" />
                            <NavBarLiItem title="Personalize your profile with video"
                                desc="Introduce yourself to new clients with Pitch" />
                        </ul>
                    </div>
                </li>
                <!-- DropMenu3  -->
                <li @mouseover="() => { isTab3 = true }" @mouseleave="() => { isTab3 = false }" class="z-20 py-3">
                    <a>Learn Design</a>
                    <div :style="{ visibility: isTab3 ? 'visible' : 'hidden' }"
                        class="fixed p-6 rounded-xl shadow-[0px_2px_30px_5px_rgba(0,0,0,0.1)] transform translate-y-2 -translate-x-8 bg-white">
                        <ul class=" flex flex-col items-start gap-5">
                            <NavBarLiItem title="Certified Product Design Course"
                                desc="Learn pro duct design in just 12 week..." />
                            <NavBarLiItem title="Browser our courses & workshops"
                                desc="Level up your skills with our interactive courses and workshops..." />
                        </ul>
                    </div>
                </li>
                <!-- DropMenu4  -->
                <li @mouseover="() => { isTab4 = true }" @mouseleave="() => { isTab4 = false }" class="z-20 py-3">
                    <a>Go Pro</a>
                    <div :style="{ visibility: isTab4 ? 'visible' : 'hidden' }"
                        class="fixed p-6 rounded-xl shadow-[0px_2px_30px_5px_rgba(0,0,0,0.1)] transform translate-y-2 -translate-x-8 bg-white">
                        <ul class=" flex flex-col items-start gap-5">
                            <NavBarLiItem title="For Designers" desc="Portfolio creation made easy" />
                            <NavBarLiItem title="For Freelancers" desc="Fresh leads in your inbox every day" />
                            <NavBarLiItem title="For Teams" desc="Build your teams pipeline or profile" />
                        </ul>
                    </div>
                </li>
                <!-- DropMenu4  -->
                <li @mouseover="() => { isTab5 = true }" @mouseleave="() => { isTab5 = false }" class="z-20 py-3">
                    <a>Marketplace</a>
                    <div :style="{ visibility: isTab5 ? 'visible' : 'hidden' }"
                        class="fixed p-6 rounded-xl shadow-[0px_2px_30px_5px_rgba(0,0,0,0.1)] transform translate-y-2 -translate-x-8 bg-white">
                        <ul class=" flex flex-col items-start gap-5">
                            <NavBarLiItem title="Discover" desc="A marketplace of digital assets..." />
                            <NavBarLiItem title="Graphics" desc="Icoms, Illustrations, Patterns, Textures..." />
                            <NavBarLiItem title="Fonts" desc="Display, Script, Sans Serif, Serif..." />
                            <NavBarLiItem title="Templates" desc="Mock Ups, Social Media, Presentations..." />
                            <NavBarLiItem title="3D" desc="Chareacters, Objects, Textures..." />
                            <NavBarLiItem title="Themes" desc="WordPress, Shopifi, Bootstrap, HTML5..." />
                            <NavBarLiItem title="Add Ons" desc="Procreate, Affinity, Photoshop, InDesign..." />
                            <hr size="1px" width="90%" />
                            <NavBarLiItem title="Open a Shop" desc="Earn money doing what you love" />
                        </ul>
                    </div>
                </li>
                <!-- DropMenu4  -->
                <li @mouseover="() => { isTab6 = true }" @mouseleave="() => { isTab6 = false }" class="z-20 py-3">
                    <a>Hire Designers</a>
                    <div :style="{ visibility: isTab6 ? 'visible' : 'hidden' }"
                        class="fixed p-6 rounded-xl shadow-[0px_2px_30px_5px_rgba(0,0,0,0.1)] transform translate-y-2 -translate-x-8 bg-white">
                        <ul class=" flex flex-col items-start gap-5">
                            <NavBarLiItem title="Designer Search" desc="Find, contact, and hire designer" />
                            <NavBarLiItem title="List my Job Opening" desc="The #1 job board for creatives" />
                            <NavBarLiItem title="Post a Freelance Project" desc="Board for freelance & contract work" />

                        </ul>
                    </div>
                </li>
            </ul>
        </div>

        <div class="flex flex-row gap-3 items-center">
            <img src="@/assets/search-icon.svg" class="h-5 w-5 hidden laptop:block" />
            <button class="text-lg">Sign in</button>
            <button
                class="bg-pink-500 rounded-lg py-2 px-3 text-sm text-white font-semibold hover:bg-pink-400 transition duration-300 ease-out hidden laptop:block">Share
                your work</button>
        </div>
    </div>
</template>


