<script setup lang="ts">
  const { profilePhoto, name, message, time } = defineProps(["profilePhoto", "name", "message", "time"])
  let photo = profilePhoto.toString()
</script>

<template>
  <div>
    <div class="flex items-center rounded-3xl bg-gray-200 mx-4">
      <div class="min-w-16 rounded-3xl bg-gray-400 m-3 overflow-hidden">
        <img v-if="profilePhoto != ''" :src="photo" alt="profile photo" class="object-cover h-16 w-16 min-h-16 min-w-16" />
        <img v-else src="../assets/gomessenger/defaults/user.svg" alt="profile photo (default)" class="object-cover h-16 w-16 min-h-16 min-w-16" />
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