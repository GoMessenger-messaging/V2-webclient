<script setup lang="ts">
  import LoginBanner from "~/components/LoginBanner.vue";

  const username = useCookie("username").value;

  const buttons = [
    {
      "to": "/chats/create",
      "icon": "/icons/plus-circle.svg",
      "text": "Create chat"
    }
  ];

  let chats: any[] = []
</script>

<template>
  <div>
    <ContentHeader title="Chats" :buttons="buttons" />
    <div v-if="username">
      <CardList v-if="chats.length != 0"/>
      <div v-else class="flex justify-center items-center">
        <h3>
          You aren't in any chat yet.
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