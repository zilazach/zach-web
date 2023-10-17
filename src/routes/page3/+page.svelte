<script>
    import { onMount } from 'svelte';

    let imgs = [];
    const BASE_URL = `https://api.unsplash.com`;
    onMount(() => {
        fetch(`${BASE_URL}/search/photos?per_page=2&query=dogs and cats&client_id=KLCfUHu8K1y3D8W_XILJ0rSKCdlCGvud5075PT3x-Yk`)
        .then(res => res.json())
        .then(data => {
            imgs = data.results;
        });
    });
</script>


{#each imgs as img}
    <img src= "{img.urls.regular}" alt="">
{/each}
