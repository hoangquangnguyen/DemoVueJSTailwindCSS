<template>
  <div class="overflow-x-hidden">
    <NavBar />
    <BannerView />
    <AllShot />
  </div>


</template>

<script lang="ts">
import { defineComponent } from 'vue';
import NavBar from './components/NavigatorBar/NavBar.vue';
import BannerView from './components/Banner/BannerView.vue';
import AllShot from './components/ShotPage/AllShot.vue';

export default defineComponent({
  name: 'App',
  components: {
    NavBar,
    BannerView,
    AllShot
  }
});
</script>

