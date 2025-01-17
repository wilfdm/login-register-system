<template>
    <div class="max-w-md mx-auto p-6 bg-white rounded-xl shadow-md space-y-4">
      <h2 class="text-2xl font-semibold text-center">Register</h2>
      <form @submit.prevent="registerUser" class="space-y-4">
        <input v-model="form.name" type="text" placeholder="Name" required class="w-full p-2 border border-gray-300 rounded-md" />
        <input v-model="form.surname" type="text" placeholder="Surname" required class="w-full p-2 border border-gray-300 rounded-md" />
        <input v-model="form.phone" type="text" placeholder="Phone" required class="w-full p-2 border border-gray-300 rounded-md" />
        <input v-model="form.email" type="email" placeholder="Email" required class="w-full p-2 border border-gray-300 rounded-md" />
        <input v-model="form.password" type="password" placeholder="Password" required class="w-full p-2 border border-gray-300 rounded-md" />
        <button type="submit" class="w-full p-2 bg-blue-500 text-white rounded-md hover:bg-blue-600">Register</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        form: {
          name: '',
          surname: '',
          phone: '',
          email: '',
          password: ''
        }
      };
    },
    methods: {
      registerUser() {
        axios.post('/register', this.form)
          .then(response => {
            alert('User registered successfully!');
          })
          .catch(error => {
            console.error('There was an error registering the user:', error);
          });
      }
    }
  };
  </script>
  