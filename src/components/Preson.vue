<template>
    <div class="person">
        <h2>姓名: {{ name }}</h2>
        <h2>年龄: {{ age }}</h2>
        <button @click="changeName">修改名字</button>
        <button @click="changeAge">修改年龄</button>
        <button @click="showTel">显示电话</button>
    </div>
</template>

<script> // 如果组件名和文件名相同，这一段可以删除，推荐是一个组件一个文件
    export default {
        name: 'Person', // 组件名
    }
</script>

<script setup>
    import { ref } from 'vue' // ref为响应式数据

    let name = ref('bruce')
    let age = ref(18)
    let tel = 111111

    function changeName() {
        name.value = 'new'  // .value是更改响应式数据的值
    }
    
    function changeAge() {
        age.value += 1
    }
    
    function showTel() {
        alert(tel)
    }
</script>

<style scoped>
    .person {
        background-color: skyblue;
        box-shadow: 0 0 10px;
        border-radius: 10px;
        padding: 20px;
    }
    button {
        margin: 0 15px;
    }
</style>