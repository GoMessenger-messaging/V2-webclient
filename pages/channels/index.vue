<script setup lang="ts">
  import LoginBanner from "~/components/LoginBanner.vue";

  const username = useCookie("username").value;

  const buttons = [
    {
      "to": "/channels/create",
      "icon": "/icons/plus-circle.svg",
      "text": "Create channel"
    },
    {
      "to": "/channels/join",
      "icon": "/icons/arrow-right-end-on-rectangle.svg",
      "text": "Join channel"
    },
    {
      "to": "/channels/discover",
      "icon": "/icons/globe-alt.svg",
      "text": "Discover channels"
    }
  ];

  let channels: any[] = []
</script>

<template>
  <div>
    <ContentHeader title="Channels" :buttons="buttons" />
    <div v-if="username">
      <CardList v-if="channels.length != 0"/>
      <div v-else class="flex justify-center items-center">
        <h3>
          You aren't in any channel yet.
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