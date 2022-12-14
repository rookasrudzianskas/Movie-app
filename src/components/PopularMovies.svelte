<script>
    export let movies;
    console.log(movies);
</script>

<h3>Popular Movies</h3>
<div class="popular-movies">
    {#each movies.results as movie}
        <h1>{movie.results}</h1>
    {/each}
</div>
