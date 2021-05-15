<template>


  <Nav />
  <Jumbo />
  <SectionOne />
  <SectionTwo />
  <SectionThree />
  <SectionFour />
  <SectionFive />
  <Footer/>


</template>

<script>
import Nav from './components/Nav.vue'
import Jumbo from './components/Jumbo.vue'
import SectionOne from './components/SectionOne.vue'
import SectionTwo from './components/SectionTwo.vue'
import SectionThree from './components/SectionThree.vue'
import SectionFour from './components/SectionFour.vue'
import SectionFive from './components/SectionFive.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Nav,Jumbo,SectionOne,SectionTwo,SectionThree,SectionFour,SectionFive,Footer
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap');

* {
margin: 0;
box-sizing: 0;
overflow-x: hidden;
font-family: 'Inter', sans-serif;
}

body{
  position: relative;
}

</style>
