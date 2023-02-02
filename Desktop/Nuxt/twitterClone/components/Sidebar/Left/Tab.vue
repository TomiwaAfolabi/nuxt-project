<template>
  <div>
    <nuxt-link
      to="#"
      class="flex items-center p-3 rounded-full w-min hover:bg-gray-200 dark:hover:bg-dim-200 dark:text-white"
      :class="defaultTransition"
    >
      <div>
        <slot class="h-8 w-8 text-dark" name="icon"></slot>
      </div>
      <div>
        <slot class="ml-4 text-xl" name="name" :class="textClasses"></slot>
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
