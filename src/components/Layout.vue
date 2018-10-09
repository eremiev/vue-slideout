<template>
    <Slideout :touch="true" :toggleSelectors="['.toggle-button']">
        <Nav/>
        <Main/>
    </Slideout>
</template>

<script>
    import Main from './Main.vue'
    import Nav from './Nav.vue'
    import Slideout from 'vue-slideout'

    export default {
        name: 'Layout',
        components: {
            Main,
            Nav,
            Slideout
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .slideout-menu {
        position: fixed;
        top: 0;
        bottom: 0;
        width: 256px;
        height: 100vh;
        /*overflow-y: scroll;*/
        -webkit-overflow-scrolling: touch;
        z-index: 0;
        display: none;
        background-color: #1D1F20;
        color: white;
    }

    .slideout-menu-left {
        left: 0;
    }

    .slideout-menu-right {
        right: 0;
    }

    .slideout-panel {
        background-color: #4B5;
        color: white;
        position: relative;
        z-index: 1;
        will-change: transform;
        min-height: 100vh;
    }

    .slideout-open,
    .slideout-open body,
    .slideout-open .slideout-panel {
        overflow: hidden;
    }

    .slideout-open .slideout-menu {
        display: block;
    }
</style>
