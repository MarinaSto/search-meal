<template>
    <div class="flex flex-col p-8">
        <div class="flex gap-2 justify-center mt-2">
            <router-link :to="{name:'byLetter',params:{letter}}" v-for="letter of letters" :key="`letter_${letter}`">
                {{ letter }}
            </router-link>
        </div>
    </div>
</template>

<script setup>
import {computed, onMounted, ref} from "vue";
import store from '../store/index.js';
import axiosClient from "../axiosClient";

const letters = 'ABCDEFGHIJLMNOPQRSTUVWXYZ'
const ingredients = ref([]);
onMounted(async () => {
    const respons = await axiosClient.get('/list.php?i=list');
})
</script>
