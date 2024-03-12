<template>
    <h1>My Movies </h1>
    <table class="table">
        <thead class="thead-dark">
        <tr>
            <th>id</th>
            <th>title</th>
            <th>body</th>
        </tr>
        </thead>
        <tbody>
        <tr v-for="movie in movies">
            <td style="width:10%">{{ movie.id }}</td>
            <td style="width:20%">{{ movie.title }}</td>
            <td style="width:70%">{{ movie.body }}</td>
        </tr>
        </tbody>
    </table>
</template>

<script setup>

import { onMounted } from "vue";
import useMovies from "../../composables/movies";

const { movies, getMovies } = useMovies()
onMounted(() => {
    getMovies()
})

</script>
