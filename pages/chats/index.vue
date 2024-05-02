<script setup lang="ts">
  import LoginBanner from "~/components/LoginBanner.vue";

  const username = useCookie("username").value;

  let chats: any[] = []
</script>

<template>
  <div>
    <div class="flex flex-col items-center m-4 mt-16">
      <h1 class="text-4xl font-extrabold">
        Chats
      </h1>
      <div class="flex mt-6">
        <div>
          <NuxtLink to="/chats/create">
            <div class="flex btn">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 9v6m3-3H9m12 0a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z" />
              </svg>
              <p class="ml-2">Create chat</p>
            </div>
          </NuxtLink>
        </div>
      </div>
    </div>
    <hr class="w-1/2 mx-auto my-8">
    <div v-if="username">
      <CardList v-if="chats.length != 0"/>
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