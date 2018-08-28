<template>
    <div>
        <Login></Login>
        <MenuA></MenuA>
        <MenuB></MenuB>
        <MenuC></MenuC>
        <Footer></Footer>
        <Navbar></Navbar>
    </div>
</template>

<script>
    import Navbar from '../public/navbar.vue'
    import Login from "./login.vue";
    import MenuA from "./menuA.vue";
    import MenuB from "./menuB.vue";
    import MenuC from "./menuC.vue";
    import Footer from '../public/footer.vue'
    export default {
        components: {
            Login,
            MenuA,
            MenuB,
            MenuC,
            Navbar,
            Footer

        }
    }
</script>