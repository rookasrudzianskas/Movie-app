<script>
    let inputValue = '';
    let active = false;
    import {goto} from '$app/navigation';

    function cancelInactive() {
        if (inputValue) {
            active = true;
        } else {
            active = false;
        }
    }

    function submitSearch(e) {
        e.preventDefault();
        goto(`/search/${inputValue}`);
    }
</script>

<form on:submit={submitSearch} class="search">

    {#if !active}
        <label for="search_movie">Search Movie</label>
    {/if}
        <input class={active ? 'selected' : ''} on:blur={cancelInactive} on:focus={() => active = true} bind:value={inputValue} type="text" name="search_movie">
    {#if inputValue}
        <button>Search</button>
    {/if}
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

    input.selected {
        background: rgb(50, 50, 50);
    }
</style>
