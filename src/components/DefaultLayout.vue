<template>
    <div class="bg-gray-50 h-full">
        <Navbar></Navbar>
        <main>
            <router-view/>
        </main>
    </div>
</template>

<script setup>
import Navbar from '../components/Navbar.vue'
</script>
