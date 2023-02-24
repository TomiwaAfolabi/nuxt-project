<template>
  <div
    class="m-2 bg-gray-50 rounded-2xl dark:bg-dim-700 overflow-hidden"
    :class="twitterBorderColor"
  >
    <h1
      class="p-3 text-gray-900 text-xl border-b font-extrabold dark:text-white"
    >
      {{ props.title }}
    </h1>

    <slot></slot>
    <div
      class="p-3 text-sm text-blue-400 cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300"
    >
      Show more
    </div>
  </div>
</template>

<script setup>
const { twitterBorderColor } = useTailwindConfig();
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
});
</script>
