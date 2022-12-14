<script>
    import {onMount} from "svelte";
    import MovieCard from "../../../components/MovieCard.svelte";
    export let movieDetail;
    onMount( async() => {
        const response = await fetch(`https://api.themoviedb.org/3/movie/436270?api_key=&language=en-US&page=1&query=parms.id&page=1&include_adult=false`);
        const data = await response.json();

        if(response.ok) {
            movieDetail = data;
        }
    })
</script>

<div class="searched-movies">
    {#each searchedMovie as movie}
        <MovieCard {movie} />
    {/each}
</div>
