
<script>
    import { onMount } from 'svelte';
    import PopularMovies from "../components/PopularMovies.svelte";
    import global from '../global.css';
    export let movies;

    onMount(async () => {
        const response = await fetch(`https://api.themoviedb.org/3/movie/popular?api_key=3d8757bd718142f06b4285fd3344456d&language=en-US&page=1`);
        const data = await response.json();

        if (response.ok) {
            movies = data;
        }
    })

</script>

<section>
    <PopularMovies {movies} />
</section>
