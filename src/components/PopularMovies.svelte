<script>
    import MovieCard from "./MovieCard.svelte";

    export let movies;

    movies = [
        {
            adult: false,
            backdrop_path: "/bQXAqRx2Fgc46uCVWgoPz5L5Dtr.jpg",
            genre_ids: (3) [28, 14, 878],
            id:436270,
            original_language: "en",
            original_title: "Black Adam",
            overview: "Nearly 5,000 years after he was bestowed with the almighty powers of the Egyptian gods—and imprisoned just as quickly—Black Adam is freed from his earthly tomb, ready to unleash his unique form of justice on the modern world.",
            popularity: 5382.38,
            poster_path: "/pFlaoHTZeyNkG83vxsAJiGzfSsa.jpg",
            release_date: "2022-10-19",
            title: "Black Adam",
            video: false,
            vote_average: 7.3,
            vote_count: 2743,
        },
        {
            adult: false,
            backdrop_path: "/bQXAqRx2Fgc46uCVWgoPz5L5Dtr.jpg",
            genre_ids: (3) [28, 14, 878],
            id:436272,
            original_language: "en",
            original_title: "Rokas Black",
            overview: "Nearly 5,000 years after he was bestowed with the almighty powers of the Egyptian gods—and imprisoned just as quickly—Black Adam is freed from his earthly tomb, ready to unleash his unique form of justice on the modern world.",
            popularity: 5382.38,
            poster_path: "/pFlaoHTZeyNkG83vxsAJiGzfSsa.jpg",
            release_date: "2022-10-19",
            title: "Rokas Black",
            video: false,
            vote_average: 7.3,
            vote_count: 2743,
        },
        {
            adult: false,
            backdrop_path: "/bQXAqRx2Fgc46uCVWgoPz5L5Dtr.jpg",
            genre_ids: (3) [28, 14, 878],
            id:436272,
            original_language: "en",
            original_title: "Rokas Black",
            overview: "Nearly 5,000 years after he was bestowed with the almighty powers of the Egyptian gods—and imprisoned just as quickly—Black Adam is freed from his earthly tomb, ready to unleash his unique form of justice on the modern world.",
            popularity: 5382.38,
            poster_path: "/pFlaoHTZeyNkG83vxsAJiGzfSsa.jpg",
            release_date: "2022-10-19",
            title: "Rokas Black",
            video: false,
            vote_average: 7.3,
            vote_count: 2743,
        },
        {
            adult: false,
            backdrop_path: "/bQXAqRx2Fgc46uCVWgoPz5L5Dtr.jpg",
            genre_ids: (3) [28, 14, 878],
            id:436272,
            original_language: "en",
            original_title: "Rokas Black",
            overview: "Nearly 5,000 years after he was bestowed with the almighty powers of the Egyptian gods—and imprisoned just as quickly—Black Adam is freed from his earthly tomb, ready to unleash his unique form of justice on the modern world.",
            popularity: 5382.38,
            poster_path: "/pFlaoHTZeyNkG83vxsAJiGzfSsa.jpg",
            release_date: "2022-10-19",
            title: "Rokas Black",
            video: false,
            vote_average: 7.3,
            vote_count: 2743,
        },
        {
            adult: false,
            backdrop_path: "/bQXAqRx2Fgc46uCVWgoPz5L5Dtr.jpg",
            genre_ids: (3) [28, 14, 878],
            id:436272,
            original_language: "en",
            original_title: "Rokas Black",
            overview: "Nearly 5,000 years after he was bestowed with the almighty powers of the Egyptian gods—and imprisoned just as quickly—Black Adam is freed from his earthly tomb, ready to unleash his unique form of justice on the modern world.",
            popularity: 5382.38,
            poster_path: "/pFlaoHTZeyNkG83vxsAJiGzfSsa.jpg",
            release_date: "2022-10-19",
            title: "Rokas Black",
            video: false,
            vote_average: 7.3,
            vote_count: 2743,
        },
        {
            adult: false,
            backdrop_path: "/bQXAqRx2Fgc46uCVWgoPz5L5Dtr.jpg",
            genre_ids: (3) [28, 14, 878],
            id:436272,
            original_language: "en",
            original_title: "Rokas Black",
            overview: "Nearly 5,000 years after he was bestowed with the almighty powers of the Egyptian gods—and imprisoned just as quickly—Black Adam is freed from his earthly tomb, ready to unleash his unique form of justice on the modern world.",
            popularity: 5382.38,
            poster_path: "/pFlaoHTZeyNkG83vxsAJiGzfSsa.jpg",
            release_date: "2022-10-19",
            title: "Rokas Black",
            video: false,
            vote_average: 7.3,
            vote_count: 2743,
        }
    ]
</script>

<h3>Popular Movies</h3>
<div class="popular-movies">
    {#each movies as movie}
        <MovieCard {movie} />
    {/each}
</div>

<style>
    h3 {
        padding: 0 1rem;
    }
    .popular-movies {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        grid-column-gap: 1rem;
        grid-row-gap: 1rem;
    }
</style>
