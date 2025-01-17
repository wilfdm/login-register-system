<template>
    <div class="max-w-md mx-auto p-6 bg-white rounded-xl shadow-md space-y-4">
      <h2 class="text-2xl font-semibold text-center">Profile</h2>
      <div v-if="user" class="space-y-2">
        <p class="text-lg"><strong>Name:</strong> {{ user.name }}</p>
        <p class="text-lg"><strong>Email:</strong> {{ user.email }}</p>
      </div>
      <div v-else class="text-center text-gray-500">
        <p>Loading...</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        user: null
      };
    },
    mounted() {
      axios.get('/profile')
        .then(response => {
          this.user = response.data;
        })
        .catch(error => {
          console.error('There was an error fetching the profile:', error);
        });
    }
  };
  </script>
  