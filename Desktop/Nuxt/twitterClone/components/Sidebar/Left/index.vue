<template>
  <div>
    <div
      class="p-2 my-2 hover:bg-blue-50 hover:rounded-full w-min dark:bg-white/20"
      :class="defaultTransition"
    >
      <div class="h-8 w-8">
        <nuxt-link to="/">
          <logo-twitter />
        </nuxt-link>
      </div>

      <SidebarLeftTab>
        <template v-slot:icon>
          <HomeIcon />
        </template>
        <template v-slot:name> Home </template>
      </SidebarLeftTab>
    </div>
  </div>
</template>
1

<script setup>
import { HomeIcon } from "@heroicons/vue/solid";

const { defaultTransition } = useTailwindConfig();
</script>
