<template>
  <div>
    <Heador></Heador>  
    <Slider></Slider>
    <Welfare></Welfare>
    <More></More>
    <Footer></Footer>
    <Navbar></Navbar>
   
  </div>
</template>

<script>
  import Heador from '../public/header.vue'
  import Slider from './bslider.vue'
  import Footer from '../public/footer.vue'
  import Navbar from '../public/navbar.vue'
  import Welfare from './welfare.vue'
  import More from './more.vue'
  

  export default {
    components: {
      Heador,
      Slider,
      Footer,
      Navbar,
      Welfare,
      More,

    }
  }
</script>