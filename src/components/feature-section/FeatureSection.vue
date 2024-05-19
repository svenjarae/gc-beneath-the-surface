<template>
  <div class="outerContainer">
    <div class="titleWrapper">
      <h1 class="title">{{ title }}</h1>
      <p class="text">{{ text }}</p>
    </div>
    <div class="gridContainer">
      <a class="box">
        <span class="icon">*</span>
        <h2 class="featureHeading">Theme one</h2>
      </a>
      <a class="box">
        <span class="icon">*</span>
        <h2 class="featureHeading">Theme two</h2>
      </a>
      <a class="box">
        <span class="icon">*</span>
        <h2 class="featureHeading">Theme three</h2>
      </a>
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
  .outerContainer {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    z-index: 2;
    width: 100%;
  }

  .titleWrapper{
    text-align: center;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 640px;
    margin-bottom: 60px;
    margin-left: auto;
    margin-right: auto;
    display: flex;
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

  .gridContainer{
    grid-auto-columns: 1fr;
    display: grid;
    grid-column-gap: 32px;
    grid-row-gap: 32px;
    grid-template-rows: auto;
    grid-template-columns: 1fr 1fr 1fr;
  }

  .box{
    cursor: pointer;
    background-color: #fff;
    border-radius: 48px;
    padding: 32px;
    text-decoration: none;
    transition: all .5s cubic-bezier(.327,-.297,.234,1.217);
    max-width: 100%;
    display: block;
    text-align: left;
  }

  .featureHeading{
    color: #000;
    margin-bottom: 8px;
    font-size: 24px;
    font-weight: 500;
    line-height: 32px;
    margin-top: 84px;
  }

  .box:hover {
    box-shadow: 0 0 20px 0 var(--orange);
    transform: scale(1.02);
  }

  .icon{
    width: 48px;
    height: 48px;
    display: block;
  }
  </style>