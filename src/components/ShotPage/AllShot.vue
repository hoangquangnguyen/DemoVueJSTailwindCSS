<script lang="ts">import { defineComponent, ref } from "vue";
import ShotItem from "./ShotItem.vue";
export default defineComponent({
    name: "AllShot",
    components: {
        ShotItem
    },
    data() {
        return {
            jobs: null
        }
    },
    methods: {

    },
    mounted() {
        fetch('http://localhost:3000/users')
            .then(res => res.json())
            .then(json => this.jobs = json)
            .catch(err => console.log(err.message))
    },
});
</script>

<template>
    <div class="flex flex-col items-center mt-3 px-10">
        <div class="">
            <button class="p-3 text-white rounded-lg bg-black hover:bg-gray-900 hidden">Fetch Data</button>
        </div>
        <div v-if="jobs != null" class="mt-3 w-full grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3  gap-8">
            <div v-for="job in jobs" :key="job['index']" class="flex-1 bg-transparent">
                <ShotItem :name="job['name']" :img="job['picture']" :like="job['longitude']" :view="job['latitude']"
                    :company="job['company']" />
            </div>
        </div>
        <div v-else="jobs==null">
            <p>Loading...</p>
            <p>If data not fetch, run json-server with command:</p>
            <p>npx json-server fakedata/db.json</p>
        </div>
    </div>

</template>