<script setup lang="ts">
  import Card from "~/components/Card.vue";

  const { list } = defineProps(["list"]);
</script>

<template>
  <div v-for="item in list">
    <div class="my-2">
      <Card :profilePhoto="item.profile_photo" :name="item.name" :message="item.last_message.message" :time="item.last_message.time"/>
    </div>
  </div>
</template>

<style scoped>

</style>