<script setup>
import {ref} from "vue";
import {onMounted} from "vue";
import ProductList from "./ProductList.vue";
let url = "https://cwpeng.github.io/live-records-samples/data/products.json";
let products = ref(null);//響應式狀態
//組件掛載後使用fetch
onMounted(async function(){
    let response = await fetch(url)
    let data = await response.json();
    products.value = data;
    console.log(data);
})
</script>
<template>  
    <div v-if="prducts===null">資料載入中</div>
    <ProductList v-else :products="products"></ProductList>
</template>
<style scoped>

</style>