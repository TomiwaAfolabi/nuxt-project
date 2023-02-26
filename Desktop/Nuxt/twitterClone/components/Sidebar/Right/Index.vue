<template>
  <div class="flex flex-col">
    <SidebarRightTab title="What's Happening">
      <SidebarPreviewCardItem
        v-for="whatsHappening in whatsHappeningItems"
        :key="whatsHappening.title"
      >
        <div>
          <h1 class="font-bold text-gray-800 text-md dark:text-white">
            {{ whatsHappening.title }}
          </h1>
          <p class="text-sm text-gray-400">{{ whatsHappening.count }}</p>
        </div>
      </SidebarPreviewCardItem>
    </SidebarRightTab>

    <SidebarRightTab title="Who to Follow">
      <SidebarPreviewCardItem
        v-for="whoToFollow in whoToFollowItems"
        :key="whoToFollow.name"
      >
        <div class="flex flex-row items-center justify-between p-2">
          <div class="flex flex-row gap-2">
            <img
              class="w-10 h-10 rounded-full"
              :src="whoToFollow.image"
              :alt="whoToFollow.name"
            />
            <div class="flex flex-col">
              <h1 class="font-bold text-gray-800 text-md dark:text-white">
                {{ whoToFollow.name }}
              </h1>
              <p class="text-sm text-gray-400">{{ whoToFollow.handle }}</p>
            </div>
          </div>
          <div class="flex h-full">
            <button
              class="text-white dark:text-black font-bold text-xs px-4 py-2 bg-black dark:bg-white rounded-full"
            >
              Follow
            </button>
          </div>
        </div>
      </SidebarPreviewCardItem>
    </SidebarRightTab>
  </div>
</template>

<script setup>
const whatsHappeningItems = ref([
  {
    title: "Space X",
    count: "18.8k Tweets",
  },
  {
    title: "#codingIsfun",
    count: "8.8k Tweets",
  },
  {
    title: "#artforall",
    count: "10.8k Tweets",
  },
]);
const whoToFollowItems = ref([
  {
    name: "Joe Biden",
    handle: "@JoeBiden",
    image: "https://picsum.photos/200",
  },
]);
</script>
