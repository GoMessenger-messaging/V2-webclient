<script setup lang="ts">
  const route = useRoute();
  const location = route.query.location;

  const usernameCookie = useCookie("username");
  const username = usernameCookie.value;

  if (username) {
    if (location) {
      navigateTo(location.toString());
    } else {
      navigateTo("/");
    }
  }
</script>

<template>
  <div>
    <h1>
      Log in
    </h1>
  </div>
</template>

<style scoped>

</style>