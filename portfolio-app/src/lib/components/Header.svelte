<script>
    import { base } from '$app/paths';
    // import Navigation.svelte from lib folder
    import { Navigation } from "$lib"
</script>

<div>
    
</div>
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
        background: #d9c300;
        background: linear-gradient(270deg, rgb(233, 210, 0) 0%, rgb(255, 230, 4) 15%, rgb(255, 227, 45) 60%, rgba(255, 245, 153, 1) 100%);
        color: rgb(0, 0, 0);
        padding: 1rem;
        position: relative;
        font-family: 'Boldonse';
        clip-path: polygon(100% 0, 100% 69%, 25% 69%, 0 100%, 0 0);
    }

    /* Logo Container */
    .logo {
        display: flex;
        align-items: center;
        z-index: 1;
        font-size: 1.5vw;
        transform: rotate(-5deg);
        padding-bottom: 1rem;
        
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