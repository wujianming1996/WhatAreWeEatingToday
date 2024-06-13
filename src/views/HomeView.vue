<template>

  <div class="container">
    <div class="tableware">
    <el-image src="src/components/img/tableware.png"  style="width: auto; height: 50%" /> 
  </div>
    <div class="foot">
 <span style="font-weight: 900;">今天吃什么？</span>
 <p style="font-weight: 500;">{{ selectedFood }}</p>
    <el-button type="warning"  @click="selectfoods" style="font-weight: 900">{{ buttonText }}</el-button>
</div>
</div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
const selectedFood = ref("");
const buttonText = ref("告诉我");
const foods = ["饺子混沌🥟","汉堡薯条🍟","意面披萨🍕","包子油条😋","麻辣烫🍲","面条🍝","日料寿司🍣","韩式料理🫕","麻辣香锅♨️","龙虾烧烤🍢","轻食沙拉🥗"];

function selectfoods() {
    const randomIndex = Math.floor(Math.random() * foods.length);
    console.log(foods[randomIndex]

    )
    selectedFood.value = foods[randomIndex];
    buttonText.value = "换一个";
    
}

</script>

<style scoped>
.container{
 display: flex;
 align-items: center;
 flex-direction: column;
 height: auto;

}
.tableware{
  padding: 100px;
}
.foot{
 display: flex;
 align-items: center;
 flex-direction: column;
 padding: 20px;

}

</style>
