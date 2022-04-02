<template>
  <form
    id="form"
    action="/choice"
    class="flex w-full gap-2 flex-wrap md:flex-nowrap"
  >
    <input
      class="py-2 px-4 focus:outline-none bg-white h-full w-full rounded-lg text-md col-span-11"
      type="search"
      name="search"
      placeholder="Search for available domains"
      v-on:blur="
        //@ts-ignore
        showDomain($event.target)
      "
      v-on:keyup.enter="
        //@ts-ignore
        showDomain($event.target)
      "
      v-on:focus="
        //@ts-ignore
        disable()
      "
    />
    <input
      id="submit"
      class="px-8 py-2 w-full md:max-w-min bg-black text-white rounded-lg text-sm col-span-1"
      type="submit"
      disabled="true"
      value="Buy"
    />
  </form>

  <div class="text-white py-2" id="availability"><br /></div>
</template>

<script lang="ts">
  import party from 'party-js';

  export default {
    name: 'Search',
    methods: {
      showDomain: async (target: { value: string }) => {
        const dmn = new URL(`http://${target.value}`).hostname;
        console.log(dmn);
        if (dmn) {
          fetch(`https://dns.cloudflare.com/dns-query?name=${dmn}&type=ns`, {
            headers: {
              accept: 'application/dns-json',
            },
          }).then(async (res) => {
            var apiResp = await res.json();
            if (apiResp.Status == 3) {
              party.confetti(document.getElementById('app')!, {
                // Specify further (optional) configuration here.
                count: party.variation.range(0, 100),
                size: party.variation.range(0.8, 2.4),
              });
              setTimeout(() => {
                (
                  document.getElementById('submit') as HTMLFormElement
                ).disabled = false;

                (
                  document.getElementById('form') as HTMLFormElement
                ).requestSubmit();
              }, 1500);
            } else {
              (
                document.getElementById('availability') as HTMLDivElement
              ).textContent = 'Domain is already used :(';
            }
          });
        } else {
          (
            document.getElementById('availability') as HTMLDivElement
          ).textContent = 'Domain entered is invalid :(';
        }
      },
      disable: () => {
        (document.getElementById('submit') as HTMLFormElement).disabled = true;
      },
    },
  };
</script>
