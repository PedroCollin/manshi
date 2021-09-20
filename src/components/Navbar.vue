<template>
    <div id="navbar" :style="cssCustom">
        <router-link to="/">Home</router-link>
        <router-link to="/history">Nossa História</router-link>
        <router-link to="/network">Rede</router-link>
        <router-link to="/work">Trabalhe Conosco</router-link>
        <router-link to="/menu">Menu</router-link>
        <img id=myLogo :src="img_logo" alt="Logo">
    </div>
</template>

<script>
export default {
    name: 'Navbar',
    props: ['text_color', 'back_color', 'img_logo'],
    computed: {
        cssCustom(){
            return {
                '--mycolor': this.text_color,
                '--myback': this.back_color,
            }
        }
    }
}
</script>

<style src="./Navbar.css">

</style>