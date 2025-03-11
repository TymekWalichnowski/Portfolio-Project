<script>
    let isOpen = false; // Menu state (open/closed)
</script>

<!-- Navigation Container-->
<nav>
    <!-- Burger menu button (visible on small screens)-->
    <button class="burger" on:click={() => isOpen = !isOpen} aria-label="Toggle navigation">
            ☰
        </button>

    <!-- Navigation links-->
    <ul>
         <li><a href="/">Home</a></li>
         <li><a href="/works">Works</a></li>
         <li><a href="/about">About</a></li>
         <li><a href="/contact">Contact</a></li>
        </ul>
</nav>


<style>
    /* Base Navigation Styling */
    .nav {
        background-color: #ff00b3;
        padding: 1rem;
        text-align: center;
    }
    nav ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        justify-content: center;
        gap: 20px; /* Adds equal spacing between items */
    }
    
    nav ul li {
        display: inline-block;
    }
    
    nav ul li a {
        text-decoration: none;
        color: white;
        font-weight: bold;
    }

        /* 🍔 Burger Menu (Hidden on Large Screens) */
        .burger {
        display: none;
        font-size: 2rem;
        background: none;
        border: none;
        cursor: pointer;
        color: white;
        position: absolute;
        top: 1rem;
        left: 1rem;
    }

    /* Mobile Navigation: Show Burger Menu */
    @media (max-width: 768px) {
        .burger {
            display: block; /* Show burger icon */
            left: 90%;
        }

        .nav ul {
            display: none; /* Hide menu by default */
            flex-direction: column;
            position: absolute;
            top: 90px;
            left: 0;
            width: 100%;
            background: #007bff;
            text-align: left;
            padding: 1rem 0;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .nav ul.open {
            display: flex; /* Show menu when isOpen is true */
        }

        .nav ul li {
            padding: 10px 20px;
        }
    }
</style>
