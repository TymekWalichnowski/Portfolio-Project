<script>
    import { onMount } from 'svelte';
    import { base } from '$app/paths';

    onMount (() => {
        console.log("About Page Loaded");
    });
</script>

<html lang="en">
<body>
    <!-- About section with named grid areas -->
    <div class= "about-container">
        <div id =about-image-container>
            <img src="{base}/20220731_011034.jpg" alt="A young bespectacled man adjusting a suit with a hawaiian shirt-tie combo underneath, he looks at the camera with a smirk" class="about-image">
        </div>
        
        <div class="about-text">
            <h1>About Me</h1>
                <p>Hi! My name is Tymoteusz Walichnowski, but you can just call me Tymek. I was born in Poland but raised in Ireland. 
                    I am a fan of all things art, but more specifically, digital art and the many ways it can be mixed with programming.  </p>
                <p>
                    I'm always willing to take new opportunities
                    and learn new things. I am knowledgable on HTML, CSS, Javascript, C++ & GDScript.</p>
            <h2>Contact Me</h2>
            <a href="mailto:tymoteuszwalichnowski@gmail.com">tymoteuszwalichnowski@gmail.com</a>
            <h3>Links</h3>
            <ul>
                <li><a href="https://www.linkedin.com/in/tymoteusz-walichnowski-819895215">LinkedIn</a></li>
                <li><a href="https://github.com/TymekWalichnowski"> GitHub</a></li>
                <li><a href="https://globalgamejam.org/users/tymekwalichnowski"> GGJ</a></li>
            </ul>
        </div>
    </div>
</body>
</html>
<style>
    
    body {
        background: #131313;
        background: linear-gradient(180deg,rgba(19, 19, 19, 1) 0%, rgba(41, 23, 40, 1) 100%);
    }
    h1 {
        font-size: 3em;
        color:#ffffff;
        padding-bottom: 1%;
        filter: drop-shadow(0 0 35px #c4c4c477); 
    }

    h2{
        filter: drop-shadow(0 0 35px #c4c4c477); 
    }

    h3{
        filter: drop-shadow(0 0 35px #c4c4c477); 
    }
    p {
        font-size: 0.8em;
        padding-bottom: 2%;
    }

    .about-container{
        width: 100vw;
        margin-top: 3%;
        display: grid;
        grid-template-columns: 1fr 1fr; /* Two columns*/
        grid-template-areas:
            "image text"
            "image aside"; /* Image spans both rows */
        gap: 20px;
        
    }

    #about-image-container {
        filter: drop-shadow(0 0 35px #ffed4b3d); 
    }
    
    .about-image {
        width: 100%;
        margin-left: 20%;
        margin-bottom: 5%;
        clip-path: polygon(10% 10%, 90% 0, 75% 100%, 0% 95%);
        border: 10px var(--primary-color);
    }
    .about-text{
        margin-left: 10%;
        margin-right: 5%;
        grid-area: text;
        text-align: right;
        font-size: 2em;
    }

    ul {
        list-style-type: none;
        list-style-position: inside;
    }

    a:hover {
        filter: drop-shadow(0 0 25px var(--primary-color)); 
    }


    @media (max-width: 980px) {
        .about-container { 
            display: flex; flex-direction: column;  
            width: 80%
        }
    .about-image { 
        order: 1; 
        

    }
    .about-text { 
        order: 2; 
        margin-left: 0%;
        text-align: center;
        font-size: 1em;
        width:100vw;
    }
    }

@media (max-width: 600px) {



}
    
</style>