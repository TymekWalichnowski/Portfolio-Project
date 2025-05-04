<script>
    // Import components
	import { Header, Footer }  from "$lib";
</script>


<!-- Header -->
<Header />


<!-- PInjects page content dynamically -->
<main>
    <slot />
</main>

<!-- Footer -->
<Footer />


<style>  
    main {
        text-align: center;
        color: white;
        background-color: var(--background-color:);
    }
</style>