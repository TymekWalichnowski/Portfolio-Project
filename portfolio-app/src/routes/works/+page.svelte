<script>
    import { onMount } from 'svelte';
    import { base } from '$app/paths';
    import { Lightbox, LightboxGallery, GalleryImage, GalleryThumbnail, i18n  } from 'svelte-lightbox';

    onMount (() => {
        console.log("Works Page Loaded");
    });

</script>

<h1>My works</h1>
<p>Have a gander through my gallery...</p>

<!-- Gallery container-->
<div class="gallery">
    <Lightbox title="Character Design for Animation"> <img src="{base}/animationCharacterFinal.png" alt="robot in street clothes shooting a gun and vaulting in an urban environment" ></Lightbox>
    <Lightbox title="Limited Palette Character Design"><img src="{base}/colourpalette5.png" alt="robed man in golden mask with blades extending out is submerged in a purple nebula"></Lightbox>
    <Lightbox title="Game-Ready Pixel Art Sprite"><img src="{base}/AllyUpIdle.gif" alt="an orange pixel art space jet-fighter thrusts forward"></Lightbox>
    <Lightbox title="3D Concept Piece"><img src="{base}/easternskyway1.png" alt="white low-poly highway amidst pink clouds with floating diamonds on square pillars"></Lightbox>
    <Lightbox title="Concept Art for Mobile Game"><img src="{base}/molegame concept art.png" alt="various character/building/enemy/world concepts for a game where western-themed miners face off against giant enemy mole characters"></Lightbox>
    <Lightbox title="Cover Art For Board Game"><img src="{base}/wonderlandwars1.png" alt="board game cover of various alice in wonderland characters fighting over the table"></Lightbox>
    <Lightbox title="Marshland Concept Art"><img src="{base}/reeds1.png" alt="A marshland of teal water and orange reeds, the sky shares the same colours and there is a cracked monument of a sphere situated in the middle of the composition"></Lightbox>
    <Lightbox title="Concept Art"><img src="{base}/PI01.png" alt="a black figure stands alone in a bright crimson-yellow subway, there is an advertisement of an octopus in the background"></Lightbox>
    <Lightbox title="Self Portrait"><img src="{base}/selfportrait.png" alt="a black and white self portrait of a teenager looking confused at the camera"></Lightbox>
    <Lightbox title="Low-Poly 3D Tree"><img src="{base}/lowpolytree.png" alt="a low poly tree with one branch sticking out"></Lightbox>
    <Lightbox title="Full Character Walk Cycle"><img src="{base}/CharacterWalkCycle.gif" alt="a sad-looking purple humanoid monster with dangly ears and a yellow chest-gemstone"></Lightbox>
    <Lightbox title="Realistic Apple Painting"><img src="{base}/ApplePainting.jpg" alt="realistic painting of an apple"></Lightbox>
    <Lightbox title="Low-Poly 3D Character Model"><img src="{base}/lemoncurator.png" alt="low poly 3d model of a cute lemon character composed of floating limbs"></Lightbox>
    <Lightbox title="Low-Poly 3D Character Model"><img src="{base}/moleranged3.png" alt="low poly mole character wearing a welding mask, is holding dynamite and also has some strapped to its belt"></Lightbox>
    <Lightbox title="2D Illustration"><img src="{base}/lifeordeath.png" alt="a masked cat humanoid is jumping from rooftop to rooftop as two masked guards chase them, the scene is entirely shades of red aside from a few white highlights"></Lightbox>
    <Lightbox title="3D Concept Piece"><img src="{base}/watertest1.png" alt="low poly 3d art of a rat character standing at a dock at daytime and smoking a cigarettes"></Lightbox>
    <Lightbox title="Character Design For Animation"><img src="{base}/turnaround1.png" alt="a 2D turnaround of a sad-looking purple humanoid monster with dangly ears and a yellow chest-gemstone"></Lightbox>
    <Lightbox title="Game-Ready Pixel Art Sprite"><img src="{base}/EnemyDownExpire.gif" alt="a green pixel art brain alien with one red eye and four blue claws looks shocked before exploding into green goo"></Lightbox>
    <Lightbox title="3D Concept Piece"><img src="{base}/zanyhijinx2.png" alt="90s cgi orange/teal checkered hillscape with floating pink cones and a big sunset"></Lightbox>
    <Lightbox title="Game-Ready Pixel Art Sprite"><img src="{base}/PowerUpInvincibility.gif" alt="pixel art of a yellow star jumping up and down and sparkling"></Lightbox>
</div>
<style>
    h1 {
        font-size: 5em;
        color:#ffffff;
        padding-top: 2%;
        padding-bottom: 1%;
        filter: drop-shadow(0 0 35px #000000); 
        filter: drop-shadow(0 0 35px #c4c4c477); 
    }

    p {
        font-size: 1.5em;
        padding-bottom: 2%;
        font-style: italic;
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
        max-width: 20vw; /* Limit the maximum width to avoid oversized images */
        margin: 1rem;
        margin-left: 1.5rem;
        margin-top: 0;
        display: block;
        width: 100%; /* Ensure the image scales to fit the images's width */
        height: auto; /* Maintain the aspect ratio */
    }

    .gallery img:hover {
        transform: translateY(-5px);
        box-shadow: 0 6px 35px rgba(230, 230, 230, 0.479);
        transform: scale(1.1); /* Scale up the hovered images */
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