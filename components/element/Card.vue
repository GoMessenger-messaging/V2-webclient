<script setup lang="ts">
  const { profilePhoto, name, message, time } = defineProps(["profilePhoto", "name", "message", "time"])
</script>

<template>
  <div>
    <div class="flex items-center rounded-3xl bg-gray-200 mx-4">
      <div class="rounded-3xl bg-gray-400 m-3">
        <img :src="{ profilePhoto }.toString()" alt="profile photo" class="h-16 min-h-16 min-w-16" />
      </div>
      <div class="truncate w-full mr-4">
        <div>
          <h3 class="truncate font-bold">{{ name }}</h3>
        </div>
        <div>
          <p class="truncate">
            {{ message }}
          </p>
        </div>
        <div>
          <p class="text-xs text-right">
            {{ time }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>