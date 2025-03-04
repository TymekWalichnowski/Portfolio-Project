<script>
    // Props allow customization of card title and description
    export let title = "Card Title";
    export let description = "This is a brief description of the card.";
</script>

<!-- Card container-->
<div class="card">
    <!-- Placeholder image-->
    <img src="placeholder.png" alt="Placeholder">

    <!-- Card content-->
    <div class ="content">
        <h2>{title}</h2>
        <p>{description}</p>
    </div>
</div>

<style>
    /* Card container with smooth hover effects */
    .card {
        background: white;
        border-radius: 10px; /* Rounded corners */
        border: 2px solid #007bff;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Subtle shadow */
        overflow: hidden;
        width: 280px;
        text-align: center;
        transition: transform 0.3s ease, box-shadow 0.3s ease; /* Smooth transitions */
    }

    /* Advanced Selector: Direct Child Combinator (>)
       This ensures that only direct `img` elements inside `.card` get these styles */
    .card > img {
        width: 100%; /* Responsive width */
        height: auto; /* Maintain aspect ratio */
        border-radius: 8px 8px 0 0; /* Round only the top corners */
    }

    /* Content Styling: Padding for better spacing */
    .content {
        padding: 1.5rem;
    }

    /* Title Styling */
    .content h2 {
        font-size: 1.2rem;
        margin-bottom: 0.5rem;
    }

    /* Description Styling */
    .content p {
        font-size: 1rem;
        color: #555;
    }

    /* Pseudo-Class: Hover Effect
       Adds a subtle lift when hovering over the card */
    .card:hover {
        transform: translateY(-5px);
        box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
    }

    /* Pseudo-Element: Adds a thin underline before the card title
       Creates a subtle decorative effect to enhance UI */
    .content h2::before {
        content: "";
        display: block;
        width: 40%;
        height: 2px;
        background: #007bff;
        margin: 0 auto 10px auto;
        transition: width 0.3s ease-in-out;
    }

    /* When .card is hovered, expand the decorative effect to 80% */
    .card:hover .content h2::before {
        width: 80%; /* Expanded width on hover */
    }
</style>
