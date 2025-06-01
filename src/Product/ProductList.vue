<script setup>
    defineProps(["products"]);
</script>
<template>
    <div>
        <table border="1">
            <tr>
                <th>產品名稱</th>
                <th>產品描述</th>
                <th>產品價格</th>
            </tr>
            <tr v-for="product in products">
                <td>{{product.name}}</td>
                <td>{{product.description}}</td>
                <td>{{product.price}}</td>                 
            </tr>
        </table>
    </div>
</template>
<style scoped>

</style>