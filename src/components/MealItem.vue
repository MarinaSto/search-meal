<template>
    <div class="bg-white shadow rounded-xl">
        <router-link :to="{name:'mealDetails',params:{id:meal.idMeal}}">
            <img :src="meal.strMealThumb" :alt="meal.strMeal" class="rounded-t-xl h-48 w-full object-cover"/>
        </router-link>
        <div class="p-3">
            <h3 class="font-bold">{{ meal.strMeal }}</h3>
            <p class="mb-4">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas id risus vitae mi ullamcorper elementum. In dictum, nisl sed pretium dictum, ante lacus ultricies tortor, sed vestibulum.
            </p>
            <YouTubeButton :href="meal.strYoutube"></YouTubeButton>
        </div>
    </div>
</template>

<script setup>
import YouTubeButton from "../components/YouTubeButton.vue";

const prop = defineProps({
    meal: Object,
})

</script>
