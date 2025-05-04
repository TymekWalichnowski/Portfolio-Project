<script>
    import { onMount } from 'svelte';
    onMount (() => {
        console.log("Contact Page Loaded");
    });
</script>
<body>
    <div>
        <h1>CV</h1>
        <h2>Jobs</h2>
        <ul>
            <li>Currently pursuing a full-time education.</li>
          </ul>
        <h2>Education</h2>
        <ul>
            <li>Southeast Technological University Carlow 2023 - Now</li>
            <ul>
                <li class="nestedlist">BSc (Hons) in Computing in Interactive Digital Art and Design.</li>
            </ul>
            <li>St Conleth's Community College 2022 - 2023 </li>
            <ul>
                <li class="nestedlist" >Level 6 Advanced Certificate in Computer Science.</li>
            </ul>
          </ul>
    </div>
</body>
<style>

    body {
        height:100%;
        background: linear-gradient(180deg,rgba(19, 19, 19, 1) 0%, rgb(29, 37, 33) 100%);
    }

    h1 {font-size: 5em;
        color:#ffffff;
        padding-top: 2%;
        padding-bottom: 1%;
        filter: drop-shadow(0 0 35px #c4c4c477); 
    }

    h2 {
        font-size: 5em;
        padding-bottom: 2%;
        padding-left: 5%;
        text-align: left;
        filter: drop-shadow(0 0 35px #c4c4c477); 
    }

    ul {
        list-style-position: inside;
        text-align: left;
    }

    li {
        font-size: 2em;
        padding-left: 5%;
    }

    .nestedlist {
        padding-left: 10%;
    }

    div {
        padding-bottom: 4%;
    }

</style>