<script setup lang="ts">
  const router = useRouter();

  const usernameCookie = useCookie("username");
  const username = usernameCookie.value;

  if (username) {
    router.back();
  }

  const buttons = [
    {
      "to": "/login",
      "icon": "/icons/arrow-right-end-on-rectangle.svg",
      "text": "Log in instead"
    }
  ];

  const inputUsername = "";
  const inputPassword = "";
  const inputPasswordConfirm = "";
  const inputEmail = "";
  const inputDisplayName = "";
</script>

<template>
  <div>
    <ContentHeader title="Sign up" :buttons="buttons" />
    <div class="flex flex-col items-center">
      <h3 class="font-bold text-xl">Sign up to GoMessenger</h3>
      <div class="rounded-2xl p-4 mt-4 bg-gray-100">
        <label for="username" class="font-bold">Username</label><br>
        <input v-model="inputUsername" type="text" id="username" class="rounded border border-gray-800"><br>
        <label for="password" class="font-bold">Password</label><br>
        <input v-model="inputPassword" type="password" id="password" class="rounded border border-gray-800"><br>
        <label for="passwordConfirm" class="font-bold">Confirm Password</label><br>
        <input v-model="inputPasswordConfirm" type="password" id="passwordConfirm" class="rounded border border-gray-800"><br>
        <label for="email" class="font-bold">Email</label><br>
        <input v-model="inputEmail" type="email" id="email" class="rounded border border-gray-800"><br>
        <label for="displayName" class="font-bold">Display name</label><br>
        <input v-model="inputDisplayName" type="text" id="displayName" class="rounded border border-gray-800"><br>
        <button type="submit" class="btn mt-4">Sign up</button>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>