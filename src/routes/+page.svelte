
<script>
    import { onMount } from 'svelte';
    import PopularMovies from "../components/PopularMovies.svelte";
    import global from '../global.css';
    import SearchMovies from "../components/SearchMovies.svelte";
    export let movies;

    onMount(async () => {
        const response = await fetch(`https://api.themoviedb.org/3/movie/popular?api_key=&language=en-US&page=1`);
        const data = await response.json();

        if (response.ok) {
            movies = data;
        }
    })

</script>

<section>
    <SearchMovies />
    <PopularMovies {movies} />
</section>
