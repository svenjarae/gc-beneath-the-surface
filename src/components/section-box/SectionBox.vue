<template>
    <div class="pageContainer">
      <div class="outerContainer">
        <h1 class="title">{{ title }}</h1>
        <h2 class="subtitle">{{ subtitle }}</h2>
        <p class="text">{{ text }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
    // Define props
    const props = defineProps({
        title: {
            type: String,
            required: true
        },
        subtitle: {
            type: String,
            required: true
        },
        text: {
            type: String,
            required: true
        }
    });

  </script>
  
  <style scoped>
  .pageContainer {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    z-index: 2;
  }
  
  .outerContainer {
    text-align: center;
  }
  
  .title {
    color: var(--silver);
    margin-bottom: 5px;
    font-family: Big Shoulders Display, sans-serif;
    font-size: 4.2rem;
    font-weight: 500;
    line-height: 4.4rem;
    text-transform: uppercase;
  }
  
  .subtitle {
    letter-spacing: 2px;
    text-transform: uppercase;
    font-family: DM Sans, sans-serif;
    font-size: 1.3rem;
    font-weight: 700;
    line-height: 1.5rem;
    color: var(--grey);
    margin-bottom: 10px;
  }
  
  .text {
    z-index: 10;
    text-align: center;
    white-space: break-spaces;
    color: var(--silver);
    margin-bottom: 10px;
    line-height: 1.4rem;
    letter-spacing: .5px;
    margin-top: 10px;
    font-size: 1rem;
  }
  </style>