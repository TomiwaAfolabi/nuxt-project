<template>
  <div :class="{ dark: darkMode }">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-screen">
        <div
          class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5"
        >
          <!-- left sidebar -->
          <div class="hidden md:block xs-col-span-1 xl:col-span-2">
            <div class="sticky top 0">
              <sidebar-left />
            </div>
          </div>

          <main class="col-span-12 bg-red-50 xl:col-span-6 md:col-span-8">
            <router-view />
          </main>
          <!--Right sidebar -->
          <div
            class="hidden col-span-12 xl:col-span-4 md:col-span-3 bg-blue-500"
          >
            <div class="sticky top 0">
              <sidebar-right />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const darkMode = ref(false);
</script>
