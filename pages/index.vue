<template>
  <div class="p-10 px-4 mx-auto max-w-4xl h-screen" id="app" style="z-index: 0">
    <div class="flex items-center justify-center">
      <img
        alt="ineedmore.domains logo"
        src="../assets/logos/vector/default.svg"
        class="w-screen"
      />
    </div>
    <div class="mt-10">
      <div class="flex items-center justify-center mb-3 w-full">
        <h2 class="text-3xl font-semibold text-white">Domain Search</h2>
      </div>
      <div class="w-full">
        <Search />
      </div>
    </div>
    <div class="mt-10">
      <div class="flex items-center justify-center mb-3 w-full">
        <h2 class="text-3xl font-semibold text-white">Cool Websites</h2>
      </div>
      <div class="flex items-center justify-center w-full">
        <Websites />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Search from "../src/components/Search.vue";
import Websites from "../src/components/Websites.vue";

export default {
  name: "App",
  components: {
    Search,
    Websites,
  },
};
</script>
