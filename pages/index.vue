<script setup lang="ts">
  const usernameCookie = useCookie("username")
  const username = usernameCookie.value
</script>

<template>
  <div class="mt-16 mx-64 p-8 rounded-3xl bg-gray-100">
    <div v-if="username" class="flex flex-col items-center">
      <h1 class="text-6xl font-extrabold">
        Welcome back, {{ username }}!
      </h1>
      <h3 class="mt-8">
        You don't have any new messages <!-- Placeholder -->
      </h3>
    </div>
    <div v-else class="flex flex-col items-center">
      <h1 class="text-6xl font-extrabold">
        Welcome!
      </h1>
      <h3 class="mt-8">
        Log in or create a new GoMessenger account
      </h3>
      <div class="flex justify-center gap-8 mt-4">
        <NuxtLink to="/login">
          <div class="btn">
            <h3>
              Log in
            </h3>
          </div>
        </NuxtLink>
        <NuxtLink to="/signup">
          <div class="btn">
            Sign up
          </div>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>