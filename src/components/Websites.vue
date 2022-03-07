<template>
  <div class="w-full h-full grid grid-cols-12 gap-2">
    <div
      class="w-full h-full col-span-12"
      v-for="website in (this || { websites }).websites"
      v-bind:key="website.href"
    >
      <a
        :href="website.href"
        class="
          flex
          px-4
          bg-white
          w-full
          h-full
          rounded-lg
          text-sm
          justify-center
          items-center
          grid grid-cols-12
          gap-1
          w-full
        "
      >
        <div class="col-span-6">{{ website.name }}</div>
        <div class="col-span-1">
          <div v-if="website.cfpages === true">
            <img
              src="https://pages.cloudflare.com/resources/logo/logo.svg"
              class="h-5 w-5"
              alt="Cloudflare Pages user"
            />
          </div>
        </div>
        <div class="col-span-1">
          <div v-if="website.cfworkers === true">
            <img
              src="https://workers.cloudflare.com/resources/logo/logo.svg"
              class="h-5 w-5"
              alt="Cloudflare Workers user"
            />
          </div>
        </div>
        <div class="col-span-1">
          <div v-if="website.contributor === true">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              alt="Contributor"
            >
              <path
                d="M12 .587l3.668 7.568 8.332 1.151-6.064 5.828 1.48 8.279-7.416-3.967-7.417 3.967 1.481-8.279-6.064-5.828 8.332-1.151z"
                fill="#f6821f"
              />
            </svg>
          </div>
        </div>
        <div class="col-span-1">
          <img
            :src="'https://github.com/' + website.user + '.png'"
            class="h-5 w-5"
          />
        </div>
        <div class="col-span-2 text-gray-700 text-xs">{{ website.username || website.user }}</div>
      </a>
      <br />
    </div>
  </div>
</template>

<script lang="ts">
// @ts-ignore
import websites from '../assets/data/websites.ts'
export default {
  name: "Websites",
  websites: Array,
  data: () => ({
    websites: websites,
  }),
};
</script>
