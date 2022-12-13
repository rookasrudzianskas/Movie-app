<script context="module">
    export async function load({fetch}) {
        // this will wait to receive the data, but as server side rendering
        const response = await fetch(`https://api.themoviedb.org/3/movie/popular?api_key=3d8757bd718142f06b4285fd3344456d&language=en-US&page=1`);
        const data = await response.json();
        console.log("This is data:", data);

        if(response.ok) {
            return {
                props: {
                    popular: data.results
                }
            };
        }
    }
</script>

<script>

</script>
