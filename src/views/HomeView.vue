<template>
  <main>
    <div class="container">
      <div v-if="backgroundImageVisible" class="bgImgContainer" :style="{ opacity: backgroundImageOpacity, transform: `scale(${backgroundImageScale})` }"></div>
      <SectionBox :opacity="sectionOpacity"></SectionBox>
    </div>
    <div style="margin-top: 100vh; height: 200vh; background-color: white;"></div>
  </main>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';
import SectionBox from '@/components/section-box/SectionBox.vue';

const initialBackgroundImageOpacity = 0.2; // Initial opacity for background image
const initialSectionOpacity = 1; // Initial opacity for section box
const maxOpacity = 1; // Max opacity for both background image and section box

const backgroundImageOpacity = ref(initialBackgroundImageOpacity); // Initial opacity set to 0.2 for background image
const sectionOpacity = ref(initialSectionOpacity); // Initial opacity set to 1 for section box
const backgroundImageVisible = ref(true); // Initial visibility of background image
const backgroundImageScale = ref(1); // Initial scale of background image

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});

function handleScroll() {
  const scrollPosition = window.scrollY;
  const fadeInEnd = 500; // End scroll position for background image fade in
  const fadeOutStart = 1000; // Start scroll position for background image fade out
  const zoomInEnd = 300; // End scroll position for zoom in effect
  const zoomOutStart = 800; // Start scroll position for zoom out effect

  if (scrollPosition <= fadeInEnd) {
    // Fade in background image
    backgroundImageOpacity.value = initialBackgroundImageOpacity + (scrollPosition / fadeInEnd) * (maxOpacity - initialBackgroundImageOpacity);
  } else if (scrollPosition >= fadeOutStart) {
    // Fade out background image
    backgroundImageOpacity.value = maxOpacity - ((scrollPosition - fadeOutStart) / (fadeInEnd * 2)) * maxOpacity;
  } else {
    // Keep background image opacity constant outside of fade in/out range
    backgroundImageOpacity.value = maxOpacity;
  }

  // Fade out section box when background image starts fading out
  sectionOpacity.value = Math.max(initialSectionOpacity - ((scrollPosition - fadeOutStart) / fadeInEnd), 0);

  // Apply zoom in/out effect
  if (scrollPosition <= zoomInEnd) {
    // Zoom in effect
    backgroundImageScale.value = 1 + (scrollPosition / zoomInEnd) * 0.2;
  } else if (scrollPosition >= zoomOutStart) {
    // Zoom out effect
    backgroundImageScale.value = 1 + ((zoomOutStart - scrollPosition) / (zoomInEnd * 2)) * 0.2;
  } else {
    // Keep background image scale constant outside of zoom in/out range
    backgroundImageScale.value = 1.2;
  }
}
</script>

<style>
.bgImgContainer {
  background-image: url('@/assets/testimg.png');
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  z-index: -1;
  transition: opacity 0.3s ease, transform 0.3s ease;
}

/* Additional styles for SectionBox component */
</style>