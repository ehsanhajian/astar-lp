<template>
  <div
    class="landscape:min-h-[500px] landscape:lg:min-h-[800px] portrait:min-h-[80vh] flex items-center justify-start"
  >
    <div class="max-w-7xl mx-auto px-4 sm:px-6 relative z-10 w-full">
      <div class="lg:w-1/2 py-12">
        <h1
          class="text-4xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight drop-shadow pt-24 sm:pt-32 lg:pt-0"
        >
          Developers
        </h1>
        <p class="text-lg sm:text-xl">
          Be part of the exciting world of multichain innovation by building EVM
          and WASM dApps on Astar Network. Astar XVM SDK is the foundation of
          our multichain smart contracts.
        </p>
        <ul
          class="hidden sm:flex justify-center sm:justify-start mt-12 space-x-2"
        >
          <li v-for="item in hero">
            <Button
              color="secondary"
              variant="contained"
              :href="item.href"
              target="_blank"
            >
              <component
                :is="item.icon"
                class="h-8 w-8 sm:mr-2 my-2"
                aria-hidden="true"
              />
              <div class="hidden sm:inline-block">{{ item.name }}</div>
              <IconArrowTopRightOnSquare
                class="w-5 h-5 stroke-2 ml-1 hidden sm:inline-block"
              />
            </Button>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const Github = resolveComponent("IconGithub");
const Discord = resolveComponent("IconDiscord");
const Docs = resolveComponent("IconDocumentation");

const hero = [
  {
    name: "GitHub",
    href: "https://github.com/AstarNetwork/Astar",
    icon: Github,
  },
  { name: "Docs", href: "https://docs.astar.network/", icon: Docs },
  { name: "Discord", href: "https://discord.gg/Z3nC9U4", icon: Discord },
];
</script>
