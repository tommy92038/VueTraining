<script setup>
    import {ref} from "vue";
    import {onMounted} from "vue";
    import ReviewList from "./ReviewList.vue"
    let url = "https://cwpeng.github.io/live-records-samples/data/reviews.json";
    let reviews = ref("null");
    onMounted(async function(){
        let response = await fetch(url);
        let data = await response.json();
        reviews.value = data;  
        console.log(data)
    });
</script>

<template>
    <div v-if="reviews===null">載入中</div>
    <ReviewList v-else :reviews="reviews"></ReviewList>
</template>

<style scoped>

</style>