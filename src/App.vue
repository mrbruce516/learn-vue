<template>
    <div class="app">
        <h1>Hello Vue</h1>
        <Preson/>
        <Car/>
    </div>
</template>

<script>
    import Car from './components/Car.vue';
import Preson from './components/Preson.vue';
    export default {
        name: 'App', // 组件名
        components: {Preson,Car} //注册组件
    }
</script>

<style>
    .app {
        background-color: #ddd;
        box-shadow: 0 0 10px;
        border-radius: 10px;
        padding: 20px;
    }
</style>