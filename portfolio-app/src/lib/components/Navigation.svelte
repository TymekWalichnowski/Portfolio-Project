<script>
    import { base } from '$app/paths';

    let isOpen = false; // Menu state (open/closed)
</script>

<!-- Navigation Container-->
<nav>
    <!-- Navigation links-->
    <ul>
         <li><a href="{base}/">Home</a></li>
         <li><a href="{base}/works">Works</a></li>
         <li><a href="{base}/about">About</a></li>
         <li><a href="{base}/cv">CV</a></li>
        </ul>
</nav>


<style>
    
    /* Base Navigation Styling */
    nav {
        text-align: center;
        
    }

    nav ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        justify-content: center;
        padding-right: 2rem;
        font-size: 2em;
    }
    
    nav ul li {
        display: inline-block;
    }
    
    nav ul li a {
        text-decoration: none;
        color: rgb(0, 0, 0);
        padding: 35px;
        font-weight: bold;
        transition: all 0.3s ease; /* Smooth transition for hover effect */
    }

    nav ul li a:hover {
        color: #ffffff; /* Change text color to white */
        background-color: #141414; /* Optional: Add a background color */
        padding-bottom: 35px; /* Add extra padding at the bottom to extend downward */

    }

    /* Mobile Navigation: Show Burger Menu */
    @media (max-width: 980px) {
        .nav ul {
            display: none; /* Hide menu by default */
            flex-direction: column;
            position: absolute;
            top: 90px;
            left: 0;
            width: 100%;
            background: #e5ff00;
            text-align: left;
            padding: 1rem 0;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            flex-grow: 1;
            font-size: 2em;
        }

        .nav ul.open {
            display: flex; /* Show menu when isOpen is true */
        }

        .nav ul li {
            padding: 10px 20px;
        }
    }

    @media (max-width: 600px) {
        nav ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        justify-content: center;
        padding-right: 2rem;
        font-size: 1em;
    }
    }
</style>
