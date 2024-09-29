<script>
    import { animate, scroll } from "motion";
	import { onMount } from "svelte";

    onMount(() => {
        scroll(
            animate(".hero p", {opacity: [1, 0], scale: [1, 1.5], display: ["block", "none"]}),
            {target: document.querySelector(".hero"), offset: ["start start", "end end"]}
        )

        scroll(
            animate(".box-grid", {gap: ["1rem", "5rem"], opacity: [1, 0], display: ["grid", "none"]}),
            {target: document.querySelector(".hero"), offset: ["start start", "end end"]}
        )
    })
</script>

<div class="body-home">
    <div style="padding: 1rem;">
        <p>The home page is currently under development</p>
        <p>Proceed to the rest of the application:</p>
        <p><span><a style="color: white;" href="login">Login</a></span> <span><a style="color: white;" href="signup">Signup</a></span></p>
    </div>
    <div class="hero">
        <p>The <span>Future</span> of Task Management<br>Starts <span>Here</span></p>
        <div class="box-grid">
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
        </div>
    </div>
    <div class="features-section">
        <p>Features</p>
        <div class="features">
            <p>feature</p>
            <p>feature</p>
            <p>feature</p>
            <p>feature</p>
        </div>
    </div>
</div>

<style>
    .features-section {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 1rem;
        flex-direction: column;
        min-height: 100vh;
    }

    .body-home {
        min-height: 100vh;
        min-height: 100svh;
        --clr-accent: #A0153E;
        font-family: sans-serif;
    }

    .hero {
        min-height: 120vh;
        max-width: 100vw;
        overflow: hidden;
        position: relative;
    }

    .hero span {
        color: var(--clr-accent);
    }

    .hero p {
        width: 100%;
        position: fixed;
        top: 50%;
        left: 50%;
        translate: -50% -50%;
        text-align: center;
        font-size: 4rem;
        z-index: 2;
    }

    .box {
        width: 100px;
        height: 100px;
        border-radius: 10px;
        background-color: #1a1a1a;
    }

    .box-grid {
        display: grid;
        grid-template-columns: repeat(8, 1fr);
        gap: 1rem;
        position: fixed;
        top: 50%;
        left: 50%;
        translate: -50% -50%;
    }

    @media (max-width: 1000px) {
        .hero p {
            font-size: 2.5rem;
        }
    }
</style>