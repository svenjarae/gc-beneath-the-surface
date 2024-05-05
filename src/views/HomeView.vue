<script setup>
  import AnimatedComponent from '@/components/animation/AnimatedComponent.vue'
  import SectionBox from '@/components/section-box/SectionBox.vue'



</script>

<template>
  <main>

    <div class="demo-container">
        <animated-component animation-type="zoom">
            <SectionBox></SectionBox>
        </animated-component>
    </div>
    
  </main>
</template>
