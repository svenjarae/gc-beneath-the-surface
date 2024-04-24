<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Cutting-Edge VR Exploration</template>
    Gran Canaria Beneath the Surface" offers a virtual window into the hidden underwater world of
    Gran Canaria, leveraging VR for immersive exploration and environmental education.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Technological Execution</template>
    Through photogrammetry and meticulous modeling using advanced software, the project creates
    lifelike 3D representations of underwater landscapes suitable for VR environments.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Educational Engagement</template>
    Interactive learning modules cover marine biology, geological formations, and environmental
    conservation, offering users a hands-on understanding of marine ecosystems.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Expert Leadership</template>
    Led by industry veterans like Anne Weigel, Philip Reinhold, and Svenja Raetzsch, the project
    combines narrative storytelling with technical expertise to deliver a captivating VR experience.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Scientific Collaboration</template>
    Collaboration with marine scientists ensures scientific accuracy, while sponsorship
    opportunities with equipment companies support the project's technical needs and promote
    environmental conservation.
  </WelcomeItem>
</template>
