<template>
    <div id="app">
        <div class="scroll-context">
            <AutoScroll>
                <div slot="autoScroll">
                    <ul>
                        <li>Coffee</li>
                        <li>Tea</li>
                        <li>Milk</li>
                        <li>Coffee</li>
                        <li>Tea</li>
                        <li>Milk</li>
                        <li>Coffee</li>
                        <li>Tea</li>
                        <li>Milk</li>
                        <li>Coffee</li>
                        <li>Tea</li>
                        <li>Milk</li>
                        <li>Coffee</li>
                        <li>Tea</li>
                        <li>Milk</li>
                        <li>Coffee</li>
                        <li>Tea</li>
                        <li>Milk</li>
                    </ul>
                </div>
            </AutoScroll>
        </div>
    </div>
</template>

<script>
    import AutoScroll from './components/AutoScroll'

    export default {
        name: 'App',
        components: {
            AutoScroll
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }

    .scroll-context {
        width: 300px;
        height: 200px;
        overflow: auto;
    }
</style>
