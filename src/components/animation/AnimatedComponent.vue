<template>
    <div 
      class="animated-content"
      :class="{ 'animate': isVisible }"
      style="will-change: opacity, transform;"
    >
      <h1 class="title" v-if="title">{{ title }}</h1>
      <h2 class="subtitle" v-if="subtitle">{{ subtitle }}</h2>
      <p class="paragraph" v-if="text">{{ text }}</p>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  import { gsap } from "gsap";
  
  const isVisible = ref(false);
  
  onMounted(() => {
    // Trigger animation when component is mounted
    isVisible.value = true;
  });
  </script>
  
  <style>
  .animated-content {
    opacity: 0;
    transform: translate3d(0px, 20px, 0px); /* Initial position */
    transition: opacity 0.5s ease, transform 0.5s ease; /* Transition animation */
  }
  
  .animate {
    opacity: 1;
    transform: translate3d(0px, 0px, 0px); /* Final position */
  }
  
  .title {
    /* Add your title styles here */
  }
  
  .subtitle {
    /* Add your subtitle styles here */
  }
  
  .paragraph {
    /* Add your paragraph styles here */
  }
  </style>