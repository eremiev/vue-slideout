<template>
    <div id="app">
        <Layout/>
    </div>
</template>

<script>
    import Layout from './components/Layout.vue'

    export default {
        name: 'app',
        components: {
            Layout
        }
    }
</script>

<style>
    body {
        width: 100%;
        height: 100%;
        margin: 0;
    }
</style>
