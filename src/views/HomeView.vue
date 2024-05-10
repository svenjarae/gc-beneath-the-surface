<template>
  <main>
    <div class="container">
      <div class="bgImgContainer"></div>
      <SectionBox></SectionBox>
    </div>

    <div>
      <AnimatedImg></AnimatedImg>
    </div>
  </main>
</template>

<script setup>
  import SectionBox from '@/components/section-box/SectionBox.vue';
  import AnimatedImg from '@/components/animation/AnimatedImg.vue';
</script>

<style>

.bgImgContainer{
  background-attachment: fixed;
  width: 100%;
  height: calc(200vh - 70px);
  opacity: 0.2;
}

</style>