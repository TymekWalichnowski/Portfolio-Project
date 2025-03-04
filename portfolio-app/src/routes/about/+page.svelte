<script>
    import { onMount } from 'svelte';

    onMount (() => {
        console.log("About Page Loaded");
    });
</script>

<h1>About Us</h1>
<!-- About section with named grid areas -->
<div class= "about-container">
    <img src="/placeholder.png" alt="About us" class="about-image">
    <div class="about-text">
        <h2>Who I am</h2>
        <p>I am an IDAD student</p>
    </div>
    <aside class="about-aside">
        <h3>My vision</h3>
        <p>Is bad and I need to wear glasses</p>
    </aside>
</div>


<style>
    h1 {color: #007bff;}

    p {font-size: 18px;}

    .about-container{
        display: grid;
        grid-template-columns: 1fr 1fr; /* Two columns*/
        grid-template-areas:
            "image text"
            "image aside"; /* Image spans both rows */
        gap: 20px;
        align-items: center;
    }

    .about-image {
        grid-area: image; /* Image spans both rows */
        width: 100%;
        border-radius: 10px;
    }

    .about-text{
        grid-area: text;
    }

    .about-aside{
        grid-area: aside;
        background: #f8f9fa;
        padding: 1rem;
        border-left: 4px solid #007bff;
        border-radius: 5px;
    }

    @media (max-width: 768px) {
        .about-container {
            grid-template-columns: 1fr;
            grid-template-areas:
                "image"
                "text"
                "aside"; /* Stacks all sections */
            text-align: center;
        }
    }
</style>