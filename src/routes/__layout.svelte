<script>import "../app.css";
    import Nav from '$lib/nav.svelte'
    import Footer from "$lib/footer.svelte";
</script>

<Nav />


<main>
<slot />
</main>

<Footer />