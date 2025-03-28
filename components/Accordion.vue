<template>
    <div class="accordion">
      <button class="accordion-header" @click="toggle">
        {{ title }}
        <span class="icon">{{ isOpen ? "▲" : "▼" }}</span>
      </button>
      <div v-if="isOpen" class="accordion-content">
        <slot></slot>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const props = defineProps({
    title: String,
  });
  
  const isOpen = ref(false);
  
  const toggle = () => {
    isOpen.value = !isOpen.value;
  };
  </script>
  
  <style scoped>
  .accordion {
    width: 100%;
    margin: 10px 0;
  }
  
  .accordion-header {
    width: 100%;
    text-align: left;
    padding: 15px;
    background: #f3f3f3;
    border: none;
    cursor: pointer;
    font-size: 1.2em;
    font-weight: bold;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .accordion-content {
    padding: 15px;
    background: white;
    border-left: 3px solid lightgreen;
  }
  
  .icon {
    font-size: 1.2em;
  }
  </style>
  