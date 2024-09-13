<template>
  <h1 class="text-center">Hello home page</h1>
  <NuxtLink to="/logins">
    <div class="flex justify-center">
      <button class="bg-red-400 p-2">Go back to login</button>
    </div>
  </NuxtLink>
</template>

<script setup>
  import { onMounted } from 'vue';
    const getDAP = async ()=> {
      try {
        const token = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3MTc0NzQ5NDAsInNlc19pZCI6IjE3IiwidXNlcl9pZCI6IjIifQ.I4zaqTFigtKciv4coR4Ogwo0KKusoWrPbGaRVinD3Fc';
        const responses = await fetch("http://192.168.11.122:3200/dashboard/analytics/customer/getDAP/1", {
          headers: {
        'Authorization': `Bearer ${token}`, // Include the token in the Authorization header
        'Content-Type': 'application/json' // Optional, depends on API requirements
      }
        })
        const data = await responses.json();
        console.log(data.data);
      }catch(err) {
        console.log(err);
      }
    }
    onMounted(getDAP);
</script>

<style lang="ts" scoped></style>
