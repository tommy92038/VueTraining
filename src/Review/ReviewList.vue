<script setup>
    defineProps(["reviews"]);
</script>
<template>
    <div>
        <table border="1">
            <tr>
                <th>產品編號</th>
                <th>評論人</th>
                <th>評論訊息</th>
                <th>星數</th>
            </tr>
            <tr v-for="review in reviews">
                <td>{{review.productNumber}}</td>
                <td>{{review.name}}</td>
                <td>{{review.message}}</td>   
                <td>{{review.star}}</td>              
            </tr>
        </table>
    </div>
</template>
<style scoped>

</style>