<!--an api used to get images of cats with dogs-->
<script>
    import { onMount } from 'svelte';

    let imgs = [];
    const BASE_URL = `https://api.unsplash.com`;
    onMount(() => {
        //async()=>{
        //    res = await fetch(`${BASE_URL}/search/photos?per_page=2&query=dogs with cats&client_id=KLCfUHu8K1y3D8W_XILJ0rSKCdlCGvud5075PT3x-Yk`)
        //    data = await res.json()
        //    imgs = data.results
        //}
        
        fetch(`${BASE_URL}/search/photos?per_page=2&query=dogs with cats&client_id=KLCfUHu8K1y3D8W_XILJ0rSKCdlCGvud5075PT3x-Yk`)
        .then(res => res.json())
        .then(data => {
            imgs = data.results;

        });
    }, 1);
</script>
<div class="contents">
<!--images from the api and the img folder-->
<div>
    {#each imgs as img}
    <img src= "{img.urls.regular}" alt="not a dino" class="page3img">
    {/each}
</div>
<br>
<div>   
    <img src= "img\fate-pets.webp" alt = "not a dino" class="page3img"> 
    <img src= "img\fate-pets-2.jpg" alt = "not a dino" class="page3img"> 
</div>
<img src="img\dogs&cats.jpg" alt="not a dino">
</div>