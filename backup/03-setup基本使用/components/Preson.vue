<template>
    <div class="person">
        <h2>姓名: {{ name }}</h2>
        <h2>年龄: {{ age }}</h2>
        <button @click="changeName">修改名字</button>
        <button @click="changeAge">修改年龄</button>
        <button @click="showTel">显示电话</button>
    </div>
</template>

<script>
    // js/ts
    export default {
        name: 'Person', // 组件名
        setup() {
            let name = 'bruce'
            let age = 18
            let tel = 111111

            function changeName() {
                name = 'new'
            }
            
            function changeAge() {
                age += 1
            }
            
            function showTel() {
                alert(tel)
            }
            return {name, age, changeName,changeAge,showTel}
        }
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