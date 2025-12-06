<template>
  <div class="card" style="width:400px; margin-top:20px;">
    <h3 class="text-small">Users List</h3>

    <p v-if="loading" class="text-small">Loading...</p>

    <ul v-else>
      <li v-for="user in users" :key="user.id" class="text-small">
        🔹 {{ user.name }}
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const users = ref([]);
const loading = ref(true);

onMounted(async () => {
  const res = await fetch("https://jsonplaceholder.typicode.com/users");
  users.value = await res.json();
  loading.value = false;
});
</script>
