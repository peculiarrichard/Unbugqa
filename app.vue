<template>
  <main>
  <Nav></Nav>
  <HeroSection></HeroSection>
  <Features></Features>
  <Audit></Audit>
  <Articles></Articles>
  <Guarantee></Guarantee>
  <Footer></Footer>
 
  </main>
  
</template>

<script setup lang="ts">
useHead({
  title: 'Unbug QA',
  meta: [
    { name: 'description', content: 'QA Testing for your startup.' }
  ],
  bodyAttrs: {
    class: 'test'
  },
})
</script>
