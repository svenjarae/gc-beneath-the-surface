<template>
  <main>
    <div class="bgImgContainer" ref="bgImgContainer"></div>
    
    <div class="container" style="background-color: black;">
      <SectionBox title="High performance injection" subtitle="subtitle" text="text"></SectionBox>
    </div>

    <div class="container">
      
    </div>

    <div class="container">
      <FeatureSection title="title" text="text"></FeatureSection>
    </div>

    <div class="container">
      <FeatureCard title="title" text="text"></FeatureCard>
    </div>
  </main>
</template>

<script setup>
  import SectionBox from '@/components/section-box/SectionBox.vue';
  import FeatureSection from '@/components/feature-section/FeatureSection.vue';
  import FeatureCard from '@/components/feature-card/FeatureCard.vue';

  import { ref, onMounted, onBeforeUnmount } from 'vue';
  import { gsap } from 'gsap';
  import { ScrollTrigger } from 'gsap/ScrollTrigger';

  gsap.registerPlugin(ScrollTrigger);

  const bgImgContainer = ref(null);

  onMounted(() => {
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: bgImgContainer.value,
        start: "top top",
        end: "+=200%", // Adjust this value based on the desired scroll length
        scrub: true,
        markers: false // Remove or set to false to hide the markers
      }
    });

    tl.fromTo(
      bgImgContainer.value,
      { opacity: 0, scale: 1 },
      { opacity: 1, scale: 1.5, duration: 1 }
    ).to(
      bgImgContainer.value,
      { opacity: 0, scale: 1, duration: 1 }
    );
  });

  onBeforeUnmount(() => {
    ScrollTrigger.getAll().forEach(trigger => trigger.kill());
  });
</script>

<style>

  .container{
    height: 100vh;
    position: relative;
    margin: auto;
  }


  .bgImgContainer {
    background-image: url('@/assets/testimg-gc.jpg'); /* Replace with your image path */
    background-size: contain;
    background-position: center;
    width: 100%;
    height: 100vh;
    position: fixed;
    top: 0;
    left: 0;
    z-index: -1;
  }

</style>