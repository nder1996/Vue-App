<template>
    <div id="app">
        <Header></Header>
        <Navbar></Navbar>
        <div class="slider container-expand-lg">
            <video src="src/assets/video/Centro.Virtual.mp4" type="video/mp4" frameborder="0" allowfullscreen autoplay loop muted></video>
        </div>
    </div>
</template>
<script>
import Header from './components/Header.vue';
import Navbar from './components/Navbar.vue';


export default {
    name: 'app',
    components: {
        Header,
        Navbar
    }
}
</script>
<style lang="scss">
#app {
    width: 100%;
    height: 100%;
    overflow: hidden;
}

.slider {
    position: relative;
    left: 1px;
}

.slider video {
    position: relative;
    width: 100%;
    left: -1px;
}
</style>