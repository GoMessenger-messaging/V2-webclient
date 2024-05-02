<script setup lang="ts">

</script>

<template>
  <div class="flex justify-between h-20 bg-gray-100 shadow-2xl shadow-gray-300">
    <div class="flex items-center">
      <NuxtLink to="/" class="px-8">
        <PageLogo />
      </NuxtLink>
      <ul class="flex gap-x-8">
        <li>
          <NuxtLink to="/chats">
            <div class="btn">
              <h3>
                Chats
              </h3>
            </div>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/channels">
            <div class="btn">
              <h3>
                Channels
              </h3>
            </div>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/communities">
            <div class="btn">
              <h3>
                Communities
              </h3>
            </div>
          </NuxtLink>
        </li>
      </ul>
    </div>
    <div class="flex items-center mr-8">
      <NuxtLink to="/account">
        <div class="btn">

        </div>
      </NuxtLink>
    </div>
  </div>
</template>

<style scoped>

</style>