<!--the layout for each page-->
<svelte:head>
    <link rel="stylesheet" href="css/main.css"/>
</svelte:head>
<script>
    import Header from "$lib/Header.svelte";
    import Footer from "$lib/Footer.svelte";
</script>

<Header/>
<slot/>
<Footer/>