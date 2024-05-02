<script setup lang="ts">
  const usernameCookie = useCookie("username")
  const username = usernameCookie.value
</script>

<template>
  <div class="flex justify-between h-20 bg-gray-100 shadow-2xl shadow-gray-300">
    <div class="flex items-center">
      <NuxtLink to="/" class="px-8">
        <PageLogo />
      </NuxtLink>
      <ul class="flex gap-8">
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
      <div v-if="username">
        <NuxtLink to="/account">
          <div class="btn">
            <h3>
              Account
            </h3>
          </div>
        </NuxtLink>
      </div>
      <div v-else class="flex gap-8">
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