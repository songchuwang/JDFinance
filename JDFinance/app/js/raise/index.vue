<template>
    <div>
        <Heador></Heador>
        <Slider></Slider>
        <Attendance></Attendance>
        <Commend></Commend>
        <Welfare></Welfare>
        <Footer></Footer>
        <Navbar></Navbar>
        
    </div>
</template>

<script>
    import Heador from '../public/header.vue'
    import Slider from './rslider.vue'
    import Footer from '../public/footer.vue'
    import Navbar from '../public/navbar.vue'
    import Attendance from './attendance.vue'
    import Commend from './commend.vue'
    import Welfare from './welfare.vue'


    export default {
        components: {
            Heador,
            Slider,
            Footer,
            Navbar,
            Attendance,
            Commend,
            Welfare,

        }
    }
</script>