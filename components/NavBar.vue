<template>
  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-icons">
        <button class="home-btn">🏠</button>
        <button class="sign-in">Sign in</button>
        <button class="register">Register</button>
        <button @click="toggleMenu" class="hamburger">
          <span v-if="!menuOpen">☰</span>
          <span v-else>✖</span>
        </button>
      </div>
      <ul v-if="menuOpen" class="menu">
        <li><a href="#">Contact Us</a></li>
        <li><a href="#">Digital Library</a></li>
        <li><a href="#">Our Collections</a></li>
        <li><a href="#">Information</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const menuOpen = ref(false);

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
};
</script>

<style scoped>
.navbar {
  position: relative;
  width: 100%;
  padding: 15px;
}

.nav-icons {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.sign-in {
  background: lightgreen;
  padding: 5px 10px;
  border-radius: 5px;
}

.register {
  background: black;
  color: white;
  padding: 5px 10px;
  border-radius: 5px;
}

.hamburger {
  font-size: 24px;
  background: none;
  border: none;
  cursor: pointer;
}

.menu {
  position: absolute;
  top: 50px;
  left: 0;
  width: 100%;
  background: lightgreen;
  padding: 10px 0;
  text-align: center;
  list-style: none;
  transition: all 0.3s ease-in-out;
}

.menu li {
  padding: 20px;
  font-size: 1.5em;
  border-bottom: 2px solid white;
}

.menu a {
  text-decoration: none;
  color: black;
}
</style>
<router-link to="/sign-in" class="sign-in">Sign in</router-link>
