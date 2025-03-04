<script>
    import { onMount } from 'svelte';

    onMount (() => {
        console.log("Contact Page Loaded");
    });
</script>

<h1>Contact Us</h1>
<p>Get in touch via email at <a href="mailto:info@example.com">infoexample.com</a>.</p>

<style>
    h1 {color: #28a745;}
    p {font-size: 18px;}
    a {color: #007bff; text-decoration: none }
    a:hover { text-decoration: underline; }
</style>