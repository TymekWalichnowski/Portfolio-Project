<script>
    import { base } from '$app/paths';
    // Props allow customization of card title and description
    export let title = "Card Title";
    export let description = "This is a brief description of the card.";
    export let image = "placeholder.png";
</script>

<!-- Card container-->
<div class="card">
    <!-- Placeholder image-->
    <img src={image} alt={title} >

    <!-- Card content-->
    <div class ="content">
        <h2>{title}</h2>
        <p>{description}</p>
    </div>
</div>

<style>
    /* Card container with smooth hover effects */
    .card {
        display: flex;
        flex-direction: column;
        background: white;
        box-shadow: 0 4px 10px rgba(255, 255, 255, 0.1); /* Subtle shadow */
        overflow: hidden;
        text-align: center;
        transition: transform 0.3s ease, box-shadow 0.3s ease; /* Smooth transitions */
        max-width: 500px; /* Limit the maximum width to avoid oversized cards */
        margin: 1rem;
    }

    /* Advanced Selector: Direct Child Combinator (>)
       This ensures that only direct `img` elements inside `.card` get these styles */
    .card > img {
        display: block;
        width: 100%; /* Ensure the image scales to fit the card's width */
        height: auto; /* Maintain the aspect ratio */
        object-fit: cover; /* Handle images gracefully */
    }

    /* Pseudo-Class: Hover Effect
       Adds a subtle lift when hovering over the card */
    .card:hover {
        transform: translateY(-5px);
        box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
    }

</style>
