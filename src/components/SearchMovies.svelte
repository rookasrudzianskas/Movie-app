<form class="search">
    <label for="search_movie">Search Movie</label>
    <input type="text" name="search_movie">
    <button>Search</button>
</form>

<style>
    .search {
        display: flex;
        flex-direction: column;
        width: 300px;
        margin: 0 auto;
    }
    .search label {
        font-size: 1.5rem;
        font-weight: bold;
        margin-bottom: 10px;
    }
    .search input {
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 5px;
        margin-bottom: 10px;
    }
    .search button {
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 5px;
        background-color: #ccc;
        cursor: pointer;
    }
</style>
