<template>
    <div class="max-w-sm mx-auto p-6 bg-white rounded-xl shadow-md space-y-4">
      <h2 class="text-2xl font-semibold text-center">Login</h2>
      <form @submit.prevent="loginUser" class="space-y-4">
        <input 
          v-model="form.email" 
          type="email" 
          placeholder="Email" 
          required 
          class="w-full p-2 border border-gray-300 rounded"
        />
        <input 
          v-model="form.password" 
          type="password" 
          placeholder="Password" 
          required 
          class="w-full p-2 border border-gray-300 rounded"
        />
        <button 
          type="submit" 
          class="w-full p-2 bg-blue-500 text-white rounded hover:bg-blue-600"
        >
          Login
        </button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        form: {
          email: '',
          password: ''
        }
      };
    },
    methods: {
      loginUser() {
        axios.post('/login', this.form)
          .then(response => {
            alert('Login successful!');
            console.log(response.data);
          })
          .catch(error => {
            console.error('There was an error logging in:', error);
          });
      }
    }
  };
  </script>
  