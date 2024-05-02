<script setup lang="ts">

</script>

<template>
  <div class="flex flex-col h-screen">
    <header>
      <PageHeader />
    </header>
    <div class="flex-grow overflow-scroll">
      <slot />
    </div>
  </div>
</template>

<style scoped>

</style>