<template>
  <div>
    <Heador></Heador>
    <Navbar></Navbar>
    <Slider></Slider>
    <Novice></Novice>
    <Borrow></Borrow>
    <Money></Money>
    <Product></Product>
    <Service></Service>
    <Footer></Footer>
    
  </div>
</template>

<script>
  import Heador from '../public/header.vue'
  import Slider from './hslider.vue'
  import Novice from './novice.vue'
  import Borrow from './borrow.vue'
  import Money from './money.vue'
  import Product from './product.vue'
  import Service from './service.vue'
  import Footer from '../public/footer.vue'
  import Navbar from '../public/navbar.vue'
  export default {
    components: {
      Heador,
      Slider,
      Novice,
      Borrow,
      Money,
      Product,
      Service,
      Footer,
      Navbar
    }
  }
</script>