<!-- eslint-disable quotes -->
<template>
  <div
    class="items-center p-3 rounded-full w-min hover:bg-gray-200 dark:hover:bg-dim-200 dark:text-white"
    :class="defaultTransition"
  >
    <nuxt-link to="#" class="flex">
      <div class="h-8 w-8 text-dark">
        <slot name="icon"></slot>
      </div>
      <div class="hidden xl:block ml-4 text-xl" :class="textClasses">
        <slot name="name"></slot>
      </div>
    </nuxt-link>
  </div>
</template>

<script setup>
const { defaultTransition } = useTailwindConfig();

const props = defineProps({
  active: {
    type: Boolean,
    default: false,
  },
});

const textClasses = computed(() => {
  return props.active ? "font-semibold" : "font-normal";
});
</script>
