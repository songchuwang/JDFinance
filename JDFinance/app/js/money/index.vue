<template>
  <div>
    <Heador></Heador>  
    <Slider></Slider>
    <Ada></Ada>
    <Money></Money>
    <Adb></Adb>
    <Choice></Choice>
    <Adc></Adc>
    <Footer cname="mfooter"></Footer>
    <Navbar></Navbar>
   
  </div>
</template>

<script>
  import Heador from '../public/header.vue'
  import Slider from './mslider.vue'
  import Footer from '../public/footer.vue'
  import Navbar from '../public/navbar.vue'
  import Ada from '../money/ada.vue'
  import Money from '../money/money.vue'
  import Adb from '../money/adb.vue'
  import Choice from '../money/choice.vue'
  import Adc from '../money/adc.vue'
  export default {
    components: {
      Heador,
      Slider,
      Footer,
      Navbar,
      Ada,
      Money,
      Adb,
      Choice,
      Adc,

    }
  }
</script>

<style lang="scss">
.mfooter{
  margin-top: 0 !important;
  section {
    div:first-child{
      display: none;
    }
  }
}
</style>
