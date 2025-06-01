<script setup>
 import ProductPage from "./Product/ProductPage.vue";
 import ReviewPage from "./Review/ReviewPage.vue"
 import {ref} from "vue";

 //響應式狀態，預設為product
 let page = ref("product");
 let change = function(clickPage){
    page.value = clickPage;
 }
</script>

<template>  
    <nav>
        <span :class="page==='product'?'current':''" @click="change('product')">產品資料</span>
        <span :class="page==='review'?'current':''" @click="change('review')">評論訊息</span>
    </nav>
    <main>
        <ProductPage v-if="page==='product'"></ProductPage>
        <ReviewPage v-if="page==='review'"></ReviewPage>
    </main>
</template>

<style scoped>
    nav{font-size:20px}
    nav>span{margin-right:10px;}
    nav>span.current{font-weight:bold}
</style>