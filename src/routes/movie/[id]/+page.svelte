<script>
    import {onMount} from "svelte";
    export let movieDetail;
    onMount( async() => {
        const response = await fetch(`https://api.themoviedb.org/3/movie/436270?api_key=&language=en-US&page=1`);
        const data = await response.json();

        if(response.ok) {
            movieDetail = data;
        }
    })
</script>

<div class="movie-details">
    <div class="img-container">
        <img src={`https://image.tmdb.org/t/p/original${movieDetail.backdrop_path}`} alt="something">
    </div>
    <div>
        <h1>{movieDetail.title}</h1>
        <p>{movieDetail.overview}</p>
        <p><span>Release Date </span>
            {movieDetail.release_date} <br />
            <span>Budget: </span> ${movieDetail.budget}
            <span>Rating: </span>
            {movieDetail.vote_average}<br />
            <span>Runtime: </span>
            {movieDetail.runtime} minutes
        </p>
    </div>
</div>

<style>
    h1 {
        padding: 1rem 0rem 2rem;
    }

    p {
        padding: 1rem 0rem;
    }

    .img-container {
        width: 100%;
    }

    img {
        width: 100%;
        border-radius: 1rem;
    }

    .movie-details {
        margin: 2rem 20%;
    }

    span {
        font-weight: bold;
    }
</style>
