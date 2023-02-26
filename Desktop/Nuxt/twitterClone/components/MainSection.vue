<template>
  <div class="border-x" :class="twitterBorderColor">
    <div
      class="sticky top-0 px-4 py-3 bg-white/80 backdrop-blur-md dark:bg-dim-900/80"
    >
      <h1 class="text-xl font-bold text-gray-800 dark:text-gray-100">
        {{ title }}
      </h1>
      <div class="flex justify-center p-4 border-b" v-if="loading">
        <UISpinner />
      </div>
      <div v-else>
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script setup>
const { twitterBorderColor } = useTailwindConfig();
const props = defineProps({
  title: {
    type: String,
    default: "",
  },
  loading: {
    type: Boolean,
    default: false,
  },
});
</script>
