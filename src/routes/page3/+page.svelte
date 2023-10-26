<!--an api used to get images of cats with dogs-->
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

<!--images from the api and the img folder-->
{#each imgs as img}
    <img src= "{img.urls.regular}" alt="not a dino" class="page3img">
{/each}
<br>
<img src= "img\fate-pets.webp" alt = "not a dino" class="page3img"> 
<img src= "img\fate-pets-2.jpg" alt = "not a dino" class="page3img"> 
<img src="img\dogs&cats.jpg" alt="not a dino">