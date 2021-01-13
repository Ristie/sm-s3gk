<template>
  <Layout>
   
    <!-- Learn how to use images here: https://gridsome.org/docs/images 
    <g-image alt="Example image" src="~/favicon.png" width="135" /> -->
   
  <About />
  <Photos />
  <Projects />
  </Layout>
</template>

<script>
import About from '@/pages/About.vue'
import Photos from '@/pages/Photos.vue'
import Projects from '@/pages/Projects.vue'


export default {

  components: {
    About,
    Photos,
    Projects
  }
}
</script>

<style>

.jumbotron {
  background: transparent;
}


.Work {
  padding: 2rem 2rem;
}

.WorkCard {
box-shadow: 0px 0px 20px rgba(0,0,0,0.1);
padding: 1rem;
border-radius: 0.2rem;
}

.Portfolioworks {
background: transparent;
color :black;
}

</style>
