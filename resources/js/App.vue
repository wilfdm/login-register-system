<template>
    <div>
      <login></login>      <!-- Login Component -->
      <register></register> <!-- Register Component -->
      <profile></profile>   <!-- Profile Component -->
    </div>
  </template>
  
  <script>
  import Login from './components/Login.vue'; // Import the Login component
  import Register from './components/Register.vue'; // Import the Register component
  import Profile from './components/Profile.vue'; // Import the Profile component
  
  export default {
    name: 'App',
    components: {
      Login,
      Register,
      Profile
    }
  };
  </script>
  
  <style scoped>
  /* Estilos opcionales */
  </style>
  