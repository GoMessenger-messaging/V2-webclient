<script setup lang="ts">

import AccountIcon from "~/components/AccountIcon.vue";
</script>

<template>
  <div class="flex justify-between h-20 bg-gray-100 shadow-2xl shadow-gray-300">
    <div class="flex items-center">
      <NuxtLink to="/" class="px-8">
        <Logo />
      </NuxtLink>
      <ul class="flex gap-x-8">
        <li class="">
          <NuxtLink to="/chats">
            <h3>
              Chats
            </h3>
          </NuxtLink>
        </li>
        <li class="">
          <NuxtLink to="/channels">
            <h3>
              Channels
            </h3>
          </NuxtLink>
        </li>
        <li class="">
          <NuxtLink to="/communities">
            <h3>
              Communities
            </h3>
          </NuxtLink>
        </li>
      </ul>
    </div>
    <div class="flex items-center">
      <NuxtLink to="/account" class="px-8">
        <AccountIcon />
      </NuxtLink>
    </div>
  </div>
</template>

<style scoped>

</style>