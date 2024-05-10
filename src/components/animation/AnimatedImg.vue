<template>
    <canvas ref="imageSequenceCanvas" />
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  import gsap from 'gsap';
  import ScrollTrigger from 'gsap/ScrollTrigger';
  
  gsap.registerPlugin(ScrollTrigger);
  
  const frameCount = 147;
  const urls = Array.from({ length: frameCount }, (_, i) => {
    return `https://www.apple.com/105/media/us/airpods-pro/2019/1299e2f5_9206_4470_b28e_08307a42f19b/anim/sequence/large/01-hero-lightpass/${(i+1).toString().padStart(4, '0')}.jpg`;
  });
  
  const imageSequenceCanvas = ref(null);
  let images = [];
  let curFrame = -1;
  let playhead = { frame: 0 };
  
  const updateImage = () => {
    const frame = Math.round(playhead.frame);
    if (frame !== curFrame) {
      const ctx = imageSequenceCanvas.value.getContext('2d');
      ctx.clearRect(0, 0, imageSequenceCanvas.value.width, imageSequenceCanvas.value.height);
      ctx.drawImage(images[Math.round(playhead.frame)], 0, 0);
      curFrame = frame;
    }
  };
  
  onMounted(() => {
    images = urls.map((url, i) => {
      const img = new Image();
      img.src = url;
      i || (img.onload = updateImage);
      return img;
    });
  
    gsap.to(playhead, {
      frame: images.length - 1,
      ease: 'none',
      onUpdate: updateImage,
      duration: images.length / 30, // assuming 30fps
      scrollTrigger: {
        start: 'top top',
        end: '+=300%', // adjust as needed
        scrub: true,
      },
    });
  });
  </script>
  
  <style>
  canvas {
    position: fixed;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    max-width: 100vw;
    max-height: 100vh;
  }
  </style>