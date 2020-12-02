<template>
  <Layout>
    <About />
    <Projects />
    <Contact />
    <Education />
    

  </Layout>
</template>

<script>
import About from '@/components/About.vue'
import Contact from '@/components/Contact.vue'
import Education from '@/components/Education.vue'
import Projects from '@/components/Projects.vue'

export default {
  metaInfo: {
    title: 'Hello, world!'
  }, 
  components: {
    About,
    Contact,
    Education,
    Projects
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
