<template>
    <tbody>
        <tr>
        <td>{{ film.episode_id }}</td>
        <td><router-link :to="'detail/' + film.episode_id">{{ film.title }}</router-link></td>
        <!-- <td>{{ film.opening_crawl }}</td> -->
        <td>{{ film.director }}</td>
        <td>{{ film.release_date }}</td>
        <!-- <td><a :href="film.url" target="_blank">{{film.url}}</a></td> -->
        </tr>
    </tbody>
</template>

<script>
    export default {
        name: 'GetApi',
        props: {
            film: Object,
            index: Number
        },
        computed: {
            
        },
    }
</script>