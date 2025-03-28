<template>
    <div class="sign-in-page">
      <NavBar />
      <main class="content">
        <h1>Sign In</h1>
  
        <form @submit.prevent="handleSignIn">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="email" placeholder="Value" required />
  
          <label for="password">Password</label>
          <input type="password" id="password" v-model="password" placeholder="Value" required />
  
          <button type="submit" class="sign-in-btn">Sign In</button>
        </form>
  
        <a href="#" class="forgot-password">Forgot password?</a>
      </main>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  import NavBar from "@/components/NavBar.vue";
  
  const email = ref("");
  const password = ref("");
  
  const handleSignIn = () => {
    console.log("Signing in with", email.value, password.value);
    // Hier kun je een API-aanroep doen voor authenticatie
  };
  </script>
  
  <style scoped>
  .sign-in-page {
    font-family: "Arial", sans-serif;
    padding: 20px;
    text-align: center;
  }
  
  .content {
    max-width: 400px;
    margin: 0 auto;
  }
  
  h1 {
    font-size: 2em;
    margin-bottom: 20px;
  }
  
  form {
    display: flex;
    flex-direction: column;
  }
  
  label {
    text-align: left;
    margin-top: 10px;
    font-weight: bold;
  }
  
  input {
    padding: 10px;
    margin: 5px 0 15px;
    border: 1px solid #ddd;
    border-radius: 5px;
    width: 100%;
  }
  
  .sign-in-btn {
    background: lightgreen;
    padding: 10px;
    border: none;
    font-size: 1em;
    cursor: pointer;
    width: 100%;
    margin-top: 10px;
    border-radius: 5px;
  }
  
  .forgot-password {
    display: block;
    margin-top: 15px;
    text-decoration: none;
    color: black;
    font-weight: bold;
  }
  </style>
  