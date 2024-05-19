<template>
  <div class="outerContainer">
    <div class="titleWrapper">
      <h1 class="title">{{ title }}</h1>
      <p class="text">{{ text }}</p>
    </div>
    <div class="gridContainer">
      <a class="card">
        <h2 class="heading">Heading</h2>
        <div class="paragraphWrapper">
          <span>Paragraph</span>
          <span>7</span>
        </div>
        <div class="paragraphWrapper">
          <span>Paragraph</span>
          <span>1</span>
        </div>
        <div class="smallImgWrapper">
          <img src="" alt="">
        </div>
        <div class="imgBg">
          <img src="" alt="">
        </div>
      </a>
      <a class="card">
        <h2 class="heading">Heading</h2>
        <div class="paragraphWrapper">
          <span>Paragraph</span>
          <span>12</span>
        </div>
        <div class="paragraphWrapper">
          <span>Paragraph</span>
          <span>12</span>
        </div>
        <div class="smallImgWrapper">
          <img src="" alt="">
        </div>
        <div class="imgBg">
          <img src="" alt="">
        </div>
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
    padding: 24px 5%;
  }

  .title{
    color: var(--silver);
    margin-bottom: 5px;
    font-family: Big Shoulders Display, sans-serif;
    font-size: 4.2rem;
    font-weight: 500;
    line-height: 4.4rem;
    text-transform: uppercase;
}

.text{
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
  
  .heading {
    color: var(--silver);
    text-align: left;
    text-transform: uppercase;
    width: auto;
    margin-bottom: 20px;
    font-family: Lato, sans-serif;
    font-size: 1.3rem;
    font-weight: 700;
    line-height: 1.5rem;
}

  .gridContainer{
    grid-auto-columns: 1fr;
    display: grid;
    grid-column-gap: 32px;
    grid-row-gap: 32px;
    grid-template-rows: auto;
    grid-template-columns: 1fr 1fr;
  }

  .card{
    background-color: var(--glass-black);
    border: 1px solid #111219;
    border-radius: 20px;
    flex-direction: column;
    align-items: left;
    width: 100%;
    min-height: 500px;
    margin-top: 20px;
    padding: 20px;
    text-decoration: none;
    transition: all .3s ease-in-out;
    display: flex;
    position: relative;
    cursor: pointer;
  }

  .card:hover{
    border: 1px solid var(--silver);
    background-color: var(--glass-black);
    outline: 0;
  }

  .paragraphWrapper {
    color: var(--silver);
    margin-bottom: 10px;
    display: inline-block;
    line-height: 1.4rem;
    letter-spacing: .5px;
    margin-top: 10px;
    margin-bottom: 0;
    font-size: 1rem;
    line-height: 1.2rem;
    text-align: left;
}

.paragraphWrapper span:nth-child(even){
  margin-left: 5px;
  font-weight: 700;
}

.smallImgWrapper{
  width: 48px;
  height: 48px;
  background-color: white;
  position: absolute;
  right: 20px;
  top: 20px;
}

  .imgBg{
    max-height: 300px;
    max-width: 300px;
    position: absolute;
    margin: auto;
    top: auto;
    bottom: 5%;
    left: 20px;
    right: 20px;
    background-color: aliceblue;
    width: auto;
    height: 100%;
    opacity: 0.2;
    border-radius: 50px;
    box-sizing: border-box;
  }
</style>