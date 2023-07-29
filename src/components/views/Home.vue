<template>
    <div class="header" >
        <h3>Popups</h3>
        <input type="submit" value="open popups" @click="openPopups">
    </div>
    <Popups v-if="isVisiblePopups" >
        <input type="submit" value="close popup" @click="openPopups">
    </Popups>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue';
import Popups from '../Popups.vue';

const isVisiblePopups = ref(false);
const openPopups = () => {
    isVisiblePopups.value = !isVisiblePopups.value;
}

onMounted(() => {
    setTimeout(() => {
        openPopups();
    },3000);
})

</script>

<style scoped>  

.header{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 30px;
    flex-direction: column;
}

input:last-of-type{
    margin-top: 30px;
}

</style>