<script setup lang="ts">
  const { title, buttons } = defineProps(["title", "buttons"])
</script>

<template>
  <div class="flex flex-col items-center m-4 mt-16">
    <h1 class="text-4xl font-extrabold">
      {{ title }}
    </h1>
    <div class="flex gap-2 mt-6">
      <div v-for="button in buttons">
        <NuxtLink :to="button.to">
          <div class="flex btn">
            <img :src="button.icon" alt="button icon" class="h-6"/>
            <p class="ml-2">{{ button.text }}</p>
          </div>
        </NuxtLink>
      </div>
    </div>
  </div>
  <hr class="w-1/2 mx-auto my-8">
</template>

<style scoped>

</style>