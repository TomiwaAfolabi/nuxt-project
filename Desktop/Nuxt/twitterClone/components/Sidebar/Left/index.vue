<template>
  <div>
    <div
      class="grid gap-2 p-2 my-2 çhover:bg-blue-50 w-min dark:bg-white/20"
      :class="defaultTransition"
    >
      <div class="h-8 w-8">
        <nuxt-link to="/">
          <logo-twitter />
        </nuxt-link>
      </div>
      <div>
        <SidebarLeftTab>
          <template v-slot:icon>
            <Icon name="home" :size="`${'30px'}`" />
          </template>
          <template v-slot:name> Home </template>
        </SidebarLeftTab>
        <SidebarLeftTab>
          <template v-slot:icon>
            <Icon name="hashtag" :size="`${'30px'}`" />
          </template>
          <template v-slot:name> HashTag </template>
        </SidebarLeftTab>
        <SidebarLeftTab>
          <template v-slot:icon>
            <Icon name="bellIcon" :size="`${'30px'}`" />
          </template>
          <template v-slot:name> Bell </template>
        </SidebarLeftTab>
        <SidebarLeftTab>
          <template v-slot:icon>
            <Icon name="inboxIcon" :size="`${'30px'}`" />
          </template>
          <template v-slot:name> Inbox</template>
        </SidebarLeftTab>
        <SidebarLeftTab>
          <template v-slot:icon>
            <Icon name="bookmarkIcon" :size="`${'30px'}`" />
          </template>
          <template v-slot:name> Bookmark </template>
        </SidebarLeftTab>
        <SidebarLeftTab>
          <template v-slot:icon>
            <Icon name="userIcon" :size="`${'30px'}`" />
          </template>
          <template v-slot:name> UserIcon </template>
        </SidebarLeftTab>
        <SidebarLeftTab>
          <template v-slot:icon>
            <Icon name="dotsCircleHIcon" :size="`${'30px'}`" />
          </template>
          <template v-slot:name> Dots </template>
        </SidebarLeftTab>
      </div>
    </div>
  </div>
</template>
<script setup>
const { defaultTransition } = useTailwindConfig();
</script>
