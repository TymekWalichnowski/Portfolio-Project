<script>
    import { onMount } from 'svelte';
    import { Card } from '$lib';

    onMount(() => {
        console.log("Home Page Loaded");
    });
</script>



<div class ="splash">
    <div>
        <img src="homeImage.jpg" alt="Man in yellow hoodie on his knee doing a cool pose outside in a LIDL carpark" id="splashImage">
    </div>
    <div>
        <h1>Welcome to my portfolio website!</h1>
        <p>Have a look around</p>
    </div>
    
</div>

<!-- Gallery container-->
<div class="gallery">
    <Card title="Card 1" description="This is the first card." />
    <Card title="Card 2" description="This is the second card." />
    <Card title="Card 3" description="This is the third card." />
    <Card title="Card 4" description="This is the fourth card." />
    <Card title="Card 5" description="This is the fifth card." />
    <Card title="Card 6" description="This is the sixth card." />
</div>

<style>
    /* splash screen styling */
    .splash {
        display:grid;
        max-width: 100vw;
        grid-template-columns: 6fr 4fr;
    }

    #splashImage {
        max-width: 100%;
        position: relative;
        left: -100px;
        animation: linear;
        animation: run;
        animation-duration: 3s;
    }

@keyframes run {
  0% {
    transform: rotate(-2deg);
    transform: translateX(-100%);
  }
  100% { 
    transform: translateX(-1fr);
   }
}

    /* Grid layout for gallery*/
    .gallery {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* responsive columns */
        gap: 40px; /* Creates spacing between items */
        margin-top: 2rem;
    }

    /* Optional: Add uniform height*/
    .gallery > .card {
        display:flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    /* Highlight the first and last child in the gallery */
    :global(.gallery > .card:first-child) {
        border: 3px solid gold; /* Emphasize the first card */
    }

    :global(.gallery > .card:last-child) {
        border: 3px solid crimson; /* Emphasize the last card */
    }

    /* Apply a different background color to even-numbered cards */
    :global(.gallery > .card:nth-child(even)) {
        background-color: #ebebeb;
    }

    /* Apply a hover effect: spotlight effect on the hovered card */
    :global(.gallery > .card:hover) {
        transform: scale(1.1); /* Scale up the hovered card */
        z-index: 2; /* Bring it to the front */
    }

    /* Reduce the size of adjacent siblings when a card is hovered */
    :global(.gallery > .card:hover ~ .card) {
        transform: scale(0.9); /* Reduce size of adjacent cards */
        opacity: 0.8; /* Slightly fade them */
    }

    /* Reduce the size of adjacent siblings when a card is hovered */
    :global(.gallery > .card:hover + .card) {
        transform: scale(0.95); /* Reduce size of adjacent cards */
        opacity: 0.9; /* Slightly fade them */
    }

    /* Apply a special styling to every third card */
    :global(.gallery > .card:nth-child(3n)) {
        border-left: 5px solid #98caff; /* Left accent border */
    }

    /* Exclude the first and last card from being affected by nth-child styling */
    :global(.gallery > .card:not(:first-child):not(:last-child)) {
        border-radius: 18px; /* Softens edges for middle cards */
    }
    
</style>