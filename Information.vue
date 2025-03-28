<template>
    <div class="information-page">
      <NavBar />
      <main class="content">
        <h1>Information</h1>
  
        <Accordion title="Opening hours">
          <p>Monday - Friday: 9 AM - 6 PM</p>
          <p>Saturday: 10 AM - 4 PM</p>
        </Accordion>
  
        <Accordion title="I’m not a student">
          <p><strong>No worries!</strong> You can still use our library.</p>
          <p><strong>Are you an alumni?</strong> Then you are a member for life!</p>
          <p><strong>Are you not an alumni?</strong> You need to become a member by paying a one-time fee of 10 euros. After paying, you’ll be a member for life!</p>
          <button class="membership-btn">⭐ Get your membership here!</button>
        </Accordion>
  
        <Accordion title="Returning books">
          <p>Books can be returned at the front desk or in the return box outside.</p>
        </Accordion>
  
        <Accordion title="Social media">
          <p>Follow us on Instagram, YouTube, and LinkedIn.</p>
        </Accordion>
      </main>
    </div>
  </template>
  
  <script setup>
  import NavBar from "@/components/NavBar.vue";
  import Accordion from "@/components/Accordion.vue";
  </script>
  
  <style scoped>
  .information-page {
    font-family: "Arial", sans-serif;
    padding: 20px;
    text-align: center;
  }
  
  .content {
    max-width: 600px;
    margin: 0 auto;
  }
  
  h1 {
    font-size: 2em;
    margin-bottom: 20px;
  }
  
  .membership-btn {
    background: lightgreen;
    padding: 10px;
    border: none;
    font-size: 1em;
    cursor: pointer;
    width: 100%;
    margin-top: 10px;
    border-radius: 5px;
  }
  </style>
  