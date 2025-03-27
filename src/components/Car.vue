<template>
    <div class="car">
        <h2>車のブランドは{{ car.brand }}，{{ car.price }}万円です</h2>
        <button @click="changePrice">価格を変更する</button>
        <br>
        <h2>ゲームライブラリ</h2>
        <ul>
            <li v-for=" game in games" :key="game.id">{{ game.name }}</li>
        </ul>
        <button @click="changeFirstGameName">ゲームを変える</button>
    </div>
</template>

<script> // 如果组件名和文件名相同，这一段可以删除，推荐是一个组件一个文件
    export default {
        name: 'Car', // 组件名
    }
</script>

<script setup>      // 自动声明setup函数和返回
    import { reactive } from 'vue';     // ref用于基本类型，reactive为对象类型
    
    let car = reactive({
        brand: 'tesla',
        price: 666
    })
    
    function changePrice() {
        car.price += 1
    }

    let games = reactive([
        {id:1,name:'lol'},
        {id:2,name:'cs:go'}
    ])
    
    function changeFirstGameName() {
        games[0].name = '原神'
    }
</script>

<style scoped>
    li {
        font-size: 20px;
    }
</style>