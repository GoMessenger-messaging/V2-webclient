<script setup lang="ts">
  const router = useRouter();

  const usernameCookie = useCookie("username");
  const username = usernameCookie.value;

  if (username) {
    router.back();
  }
</script>

<template>
  <div>
    <h1>
      Sign up
    </h1>
  </div>
</template>

<style scoped>

</style>