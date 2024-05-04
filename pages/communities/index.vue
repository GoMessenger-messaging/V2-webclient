<script setup lang="ts">
  import LoginBanner from "~/components/LoginBanner.vue";

  const username = useCookie("username").value;

  const buttons = [
    {
      "to": "/communities/create",
      "icon": "/icons/plus-circle.svg",
      "text": "Create community"
    },
    {
      "to": "/communities/join",
      "icon": "/icons/arrow-right-end-on-rectangle.svg",
      "text": "Join community"
    },
    {
      "to": "/communities/discover",
      "icon": "/icons/globe-alt.svg",
      "text": "Discover communities"
    }
  ];

  let communities: any[] = []
</script>

<template>
  <div>
    <ContentHeader title="Communities" :buttons="buttons" />
    <div v-if="username">
      <CardList v-if="communities.length != 0"/>
      <div v-else class="flex justify-center items-center">
        <h3>
          You aren't in any community yet.
        </h3>
      </div>
    </div>
    <div v-else>
      <LoginBanner />
    </div>
  </div>
</template>

<style scoped>

</style>