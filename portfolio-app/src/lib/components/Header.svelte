<script>
    // import Navigation.svelte from lib folder
    import { Navigation } from "$lib"
</script>


<header>
    <!-- Logo -->
    <div class="logo">
        <h1>Tymek W.</h1>
    </div>

    <!-- Navigation -->
    <Navigation />
</header>

<style>
    /* Header Styling */
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background: linear-gradient(to bottom right, var(--primary-color) 50%, transparent 50%), var(--primary-color);
        color: rgb(0, 0, 0);
        padding: 1rem;
        position: relative;
        overflow: visible; 
        font-family: 'Boldonse';

    }

    /* Logo Container */
    .logo {
        display: flex;
        align-items: center;
        z-index: 1;
        font-size: 2em;
    }

    /* Mobile: Center logo and stack items */
    @media (max-width: 980px) {
        header {
            flex-direction: column;
            text-align:center;
            clip-path: polygon(100% 0, 100% 76%, 0 76%, 0 0);
        }

        .logo {
            justify-content: center;
            display:none;
        }
    }

    @media (max-width: 600px) {

}
</style>