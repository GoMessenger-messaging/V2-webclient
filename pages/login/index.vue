<script setup lang="ts">
  const router = useRouter();

  const usernameCookie = useCookie("username");
  const username = usernameCookie.value;

  if (username) {
    router.back();
  }

  const buttons = [
    {
      "to": "/signup",
      "icon": "/icons/user-plus.svg",
      "text": "Sign up instead"
    }
  ];

  const inputUsername = "";
  const inputPassword = "";
</script>

<template>
  <div>
    <ContentHeader title="Log in" :buttons="buttons" />
    <div class="flex flex-col items-center">
      <h3 class="font-bold text-xl">Log in to GoMessenger</h3>
      <div class="rounded-2xl p-4 mt-4 bg-gray-100">
        <label for="username" class="font-bold">Email or username</label><br>
        <input v-model="inputUsername" type="text" id="username" class="rounded border border-gray-800"><br>
        <label for="password" class="font-bold">Password</label><br>
        <input v-model="inputPassword" type="password" id="password" class="rounded border border-gray-800"><br>
        <button type="submit" class="btn mt-4">Log in</button>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>