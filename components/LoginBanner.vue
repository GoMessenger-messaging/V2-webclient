<script setup lang="ts">

</script>

<template>
  <div class="flex flex-col items-center mx-96 p-4 rounded-3xl bg-gray-100">
    <h3 class="mt-8 font-bold text-3xl">
      You need to log in first
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
</template>

<style scoped>

</style>