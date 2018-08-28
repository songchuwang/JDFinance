<template>
    <div>
        <Login></Login>
        <MenuA></MenuA>
        <Footer></Footer>
        <Navbar></Navbar>
    </div>
</template>

<script>
    import Navbar from '../public/navbar.vue'
    import Login from "./login.vue";
    import MenuA from "./menuA.vue";
    import Footer from '../public/footer.vue'
    export default {
        components: {
            Login,
            MenuA,
            Navbar,
            Footer

        }
    }
</script>