<script>
    import { onMount } from 'svelte';
    import { Card } from '$lib';
    import { Lightbox, LightboxGallery, GalleryImage, GalleryThumbnail, i18n  } from 'svelte-lightbox';

    onMount (() => {
        console.log("Works Page Loaded");
    });

</script>

<h1>My works</h1>
<p>All my art is featured here</p>

<!-- Gallery container-->

<div class="gallery">
    <Lightbox title="Character Design for Animation"> <img src="works\animationCharacterFinal.png" alt="test" ></Lightbox>
    <Lightbox title="Limited Palette Character Design"><img src="works\colourpalette5.png" alt=" "></Lightbox>
    <Lightbox title="Game-Ready Pixel Art Sprite"><img src="works\AllyUpIdle.gif" alt=" "></Lightbox>
    <Lightbox title="3D Concept Piece"><img src="works\easternskyway1.png" alt=" "></Lightbox>
    <Lightbox title="Concept Art for Mobile Game"><img src="works\molegame concept art.png" alt=" "></Lightbox>
    <Lightbox title="Marshland Concept Art"><img src="works\reeds1.png" alt=" "></Lightbox>
    <Lightbox title="Low-Poly 3D Tileset"><img src="works\tileset.png" alt=" "></Lightbox>
    <Lightbox title="Concept Art"><img src="works\PI01.png" alt=" "></Lightbox>
    <Lightbox title="Low-Poly 3D Character Model"><img src="works\lemoncurator.png" alt=" "></Lightbox>
    <Lightbox title="Low-Poly 3D Character Model"><img src="works\moleranged3.png" alt=" "></Lightbox>
    <Lightbox title="Character Design For Animation"><img src="works\turnaround1.png" alt=" "></Lightbox>
    <Lightbox title="Game-Ready Pixel Art Sprite"><img src="works\EnemyDownExpire.gif" alt=" "></Lightbox>
    <Lightbox title="3D Concept Piece"><img src="works\watertest1.png" alt=" "></Lightbox>
    <Lightbox title="3D Concept Piece"><img src="works\zanyhijinx2.png" alt=" "></Lightbox>
</div>

<style>
    h1 {
        font-size: 5em;
        color:#ffffff;
        padding-top: 2%;
        padding-bottom: 1%;
        filter: drop-shadow(0 0 35px #000000); 
    }

    p {
        font-size: 1.5em;
        padding-bottom: 2%;
    }


    .gallery {
        columns: 4;
        padding-bottom: 2%;
        margin:auto;
    }

    .gallery img {
        display: flex;
        flex-direction: column;
        background: white;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Subtle shadow */
        overflow: hidden;
        transition: transform 0.3s ease, box-shadow 0.3s ease; /* Smooth transitions */
        max-width: 20vw; /* Limit the maximum width to avoid oversized cards */
        margin: 1rem;
        margin-top: 0;
        display: block;
        width: 100%; /* Ensure the image scales to fit the card's width */
        height: auto; /* Maintain the aspect ratio */
    }

    .gallery img:hover {
        transform: translateY(-5px);
        box-shadow: 0 6px 15px rgba(230, 230, 230, 0.15);
        transform: scale(1.1); /* Scale up the hovered card */
        z-index: 1; /* Bring it to the front */
    }

    @media (max-width: 600px) {
        .gallery {
            columns: 2;
            max-width:60vw;
           align-items: center;
    }
}
</style>