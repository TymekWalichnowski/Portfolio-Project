<script>
    import { onMount } from 'svelte';
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    import '@splidejs/svelte-splide/css';
    import { goto } from '$app/navigation';
    import { Card } from '$lib';

    onMount(() => {
        console.log("Home Page Loaded");
    });


</script>



<div class ="splash">
    <div>
        <img src="works\godotfire.gif" alt="Yellow sky way" id="splashImage">
    </div>
    <div class = "splashtext">
        <h1 >Welcome to my portfolio!</h1>
        <p>Have a look around!</p>
    </div>
    
</div>

<div id="featuredtext">
    <h2>Featured Works:</h2>
</div>

<section id ="slides">
<Splide options={ { rewind: true, perPage: 3, perMove: 1, type   : 'loop',
 autoplay: true , interval: 3000, autoWidth: true, focus: 'center', gap: '5rem'
} } aria-label="Svelte Splide Example">
     <SplideSlide>
        <img class ="slideImage" src="\works\easternskyway1.png" alt="Image 1"/>
      </SplideSlide>
    <SplideSlide>
        <img class ="slideImage" src="works\animationCharacterFinal.png" alt="Image 2"/>
    </SplideSlide>
    <SplideSlide>
        <img class ="slideImage" src="works\lemoncurator.png" alt="Image 2"/>
    </SplideSlide>
    <SplideSlide>
      <img class ="slideImage" src="\works\zanyhijinx2.png" alt="Image 2"/>
    </SplideSlide>
    <SplideSlide>
        <img class ="slideImage" src="works\watertest1.png" alt="Image 2"/>
    </SplideSlide>
    <SplideSlide>
        <img class ="slideImage" src="\works\moleranged3.png" alt="Image 1"/>
      </SplideSlide>

  </Splide>
</section>

<div id="middlespace">


<div id="projectstext">
    <h2>Projects I've worked on:</h2>
</div>

<div class="projectshowcase">
    <img src="games\rhythmgamevid.gif" alt="Yellow sky way">
    <div>
        <h3>Rhythm Game:</h3>
        <ul>
            <li>Fun & Engaging Rhythm-based gameplay</li>
            <li>All programming, art & assets made solo</li>
            <li>Coded entirely with C++ in SFML</li>
          </ul>
    </div>
</div>

<div class="projectshowcase2">
    <div>
        <h3>Versus Roulette:</h3>
        <ul>
            <li>Mix of strategy and luck-based gameplay</li>
            <li>Team Leader, handled coding certain game elements and directing trailer</li>
            <li>Coded entirely with C++ in SFML</li>
          </ul>
    </div>
    <img src="games\versusroulette.png" alt="Yellow sky way">
</div>

<div class="projectshowcase">
    <img src="games\rushtoriches.png" alt="Yellow sky way">
    <div>
        <h3>Rush to Riches: Before the Bubble Bursts:</h3>
        <ul>
            <li>Buy property & Stocks and amass as much wealth as possible before the financial bubble bursts</li>
            <li>Team Leader, handled concept and coding aspects</li>
            <li>Coded entirely within Godot</li>
          </ul>
    </div>


</div>
<div id="endspace">
    <button on:click={() => goto('/works')}>See my other works!</button>
    <button on:click={() => goto('/about')}>Contact Me!</button>
</div>
</div>

<style>

    .projectshowcase, .projectshowcase2 {
        display:grid;
        grid-template-columns: 3fr 2fr; 
        margin-bottom: 2%;
        font-size: 2em;
        color:#363636;
        font-family: 'Press Start 2P';
        
    }

    .projectshowcase2 {
        grid-template-columns: 2fr 3fr; 
    }

    .projectshowcase img, .projectshowcase2 img {
    width: 100%;
    height: 100%;
    clip-path: polygon(0 0, 100% 0, 80% 100%, 0 100%);
    }

    .projectshowcase2 img {
        clip-path: polygon(0 0, 100% 0, 100% 100%, 20% 100%);
    }

    .projectshowcase div, .projectshowcase2 div {
    display: flex;
    flex-direction: column;
    justify-content: center;
}

    .projectshowcase h3, .projectshowcase2 h3 {
        font-size: 1.17em;
        color:black;
     }

    ul {
        list-style-position: inside;
        font-weight: 600;
    }

    li {
        margin: 10% 0;
    }

    #slides {
        filter: drop-shadow(0 0 50px rgba(56, 56, 56, 0.473)); 
    }
    #projectstext {
        font-size: 2rem;
        color:#000000;
        padding-top: 7%;
        padding-bottom: 5%;
        filter: drop-shadow(0 0 35px #000000); 
        font-family: 'Press Start 2P';
    }

    /* splash screen styling */
    .splash {
        display:grid;
        max-width: 100vw;
        margin-top: 2%;
        grid-template-columns: 5fr 3fr;
        justify-content: center;
        height: 50%;
        background: #18171A;
background: linear-gradient(180deg, rgba(24, 23, 26, 0) 0%, rgba(207, 207, 207, 0.25) 50%, rgba(24, 23, 26, 0) 100%);
    }

    .splashtext {
        font-size: 2rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: left;
    }

    #splashImage {
        max-width: 100%;
        position: relative;
        left: -30px;
        animation: linear;
        animation: run;
        animation-duration: 3s;
        clip-path: polygon(0 0, 100% 0, 80% 100%, 0 100%);
    }

    #featuredtext {
        text-align: left;
        font-size: 2rem;
        padding-top: 2%;
        padding-bottom: 2%;
        filter: drop-shadow(0 0 35px rgba(224, 224, 224, 0.164)); 
        padding-left: 3%;
        font-style: italic;
    }

    .slideImage{
        height: 30rem;
  }

  #middlespace {
    margin-top: 1%;
    padding-top: 5%;
    background: #e0ddd5;
background: linear-gradient(0deg, rgba(224, 221, 213, 1) 0%, rgba(217, 214, 158, 1) 50%, rgba(189, 189, 57, 1) 100%);
    clip-path: polygon(0 4%, 100% 2%, 100% 100%, 0% 100%);
    z-index: 1;
    
  }
  #endspace {
    padding-top: 10%;
    padding-bottom: 10%;
    display: grid;
    justify-content: center;
    gap: 6rem;
    background: #626235;
    background: linear-gradient(180deg,rgba(98, 98, 53, 1) 0%, rgba(20, 19, 17, 1) 100%);
    clip-path: polygon(0 0, 100% 10%, 100% 100%, 0% 100%);
    z-index: 2;
  }

  button {
    border-style: solid;
    background-color: var(--primary-color);
    color: var(--primary-color);
    border-color: var(--primary-color);
    color: black;
    font-size: 3rem;
    font-weight: bold;
    padding: 2rem;
    border-radius: 45px;
    cursor: pointer;
    transition: all 0.2s ease;
    filter: drop-shadow(0 0 20px rgb(0, 0, 0)); 
  }

  button:hover {
    color: white;
    filter: drop-shadow(0 0 30px rgb(254, 255, 166)); 
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

@media (max-width: 980px) {
        .splash {
            display:grid;
            max-width: 100vw;
            grid-template-columns: 5fr 3fr;
            justify-content: center;
            height: 50%;
        }

        .splashtext {
            font-size: 1rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            text-align: left;
        }

        #featuredtext {
            text-align: center;
            font-size: 1.5rem;
            padding-top: 3%;
            padding-bottom: 3%;
        }

            .slideImage{
                height: 12rem;
        }

        #projectstext {
        font-size: 1.5rem;
        padding-top: 2%;
        padding-bottom: 2%;
    }

    }

    @media (max-width: 600px) {
        .splashtext {
            font-size: 0.5rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            text-align: left;
        }

        .projectshowcase, .projectshowcase2{
            font-size: 1em;
        }
        .projectshowcase h3 {
            font-size: 1.17em;
        }


    }
</style>