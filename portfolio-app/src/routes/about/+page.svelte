<script>
    import { onMount } from 'svelte';

    onMount (() => {
        console.log("About Page Loaded");
    });
</script>
<html>
</html>

    <!-- About section with named grid areas -->
    <div class= "about-container">
        <img src="/real/20220731_011034.jpg" alt="About us" class="about-image">
        <div class="about-text">
            <h1>About Me</h1>
                <p>Hi! My name is Tymoteusz Walichnowski, but you can just call me Tymek. I was born in Poland but raised in Ireland. 
                    I am a fan of all things art, but more specifically, digital art.  </p>
                <p>
                    I'm always willing to take new opportunities
                    and learn new things. I am knowledgable on HTML, CSS, Javascript, C++ & GDScript.</p>
            <h2>Contact Me</h2>
            <a href="mailto:tymoteuszwalichnowski@gmail.com">tymoteuszwalichnowski@gmail.com</a>
            <h3>Links</h3>
            <ul>
                <li><a href="https://www.linkedin.com/in/tymoteusz-walichnowski-819895215">LinkedIn</a></li>
                <li><a href="https://github.com/TymekWalichnowski">GitHub</a></li>

            </ul>

        </div>
    </div>

<style>
    
    html {
        background: #131313;
        background: linear-gradient(180deg,rgba(19, 19, 19, 1) 0%, rgba(41, 23, 40, 1) 100%);
    }
    h1 {
        font-size: 3em;
        color:#ffffff;
        padding-bottom: 1%;
        filter: drop-shadow(0 0 35px #000000); 
    }

    p {
        font-size: 0.8em;
        padding-bottom: 2%;
    }

    .about-container{
        margin-top: 3%;
        display: grid;
        grid-template-columns: 1fr 1fr; /* Two columns*/
        grid-template-areas:
            "image text"
            "image aside"; /* Image spans both rows */
        gap: 20px;
        
    }

    .about-image {
        grid-area: image; /* Image spans both rows */
        width: 40rem;
        margin-left: 20%;
        margin-bottom: 5%;
        clip-path: polygon(10% 10%, 90% 0, 75% 100%, 0% 95%);
        border: 10px var(--primary-color);
        padding: 10px;
    }
    .about-text{
        margin-right: 5%;
        grid-area: text;
        text-align: right;
        font-size: 2em;

    }

    ul {
        list-style-type: none;
        list-style-position: inside;
    }



    .about-aside{
        grid-area: aside;
        background: #494949;
        padding: 1rem;
        border-left: 4px solid var(--primary-color);
        border-radius: 5px;

    }

    @media (max-width: 980px) {
        
    }

@media (max-width: 600px) {



}
    
</style>