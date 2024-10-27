<script>
    import Available from '$lib/components/Available.svelte';
	import About from '$lib/components/About.svelte';
	import Experience from '$lib/components/Experience.svelte';
    import Skills from '$lib/components/Skills.svelte';
    import Projects from '$lib/components/Projects.svelte';
    import Articles from '$lib/components/Articles.svelte';
    import Intro from '$lib/components/Intro.svelte';
</script>

<svelte:head>
    <title>Walter O'Brien</title>
</svelte:head>

<main>
    <div class="intro-content">
        <Intro />
    </div>
    <div class="resume-content">
        <div class="left-column">
            <div class="left-inner-top">
                <div class="left-inner-top-inner-column">
                    <Available />
                </div>
                <div class="left-inner-top-inner-column">
                    <About />
                </div>
            </div>
            <div class="left-inner-bottom">
                <Experience />
            </div>
        </div>
    
        <div class="right-column">
            <div class="right-inner-top">
                <Skills />
            </div>
            <div class="right-inner-middle">
                <Projects />
            </div>
            <div class="right-inner-bottom">
                <Articles />
            </div>
        </div>
    </div>
</main>

<style>
    .intro-content, .resume-content {
        display: flex;
        flex-direction: row;
        gap: 2rem;
        width: 90%;
        margin: 0 auto;
        height: max-content;
    }

    .resume-content {
        justify-content: space-evenly;
    }

    .left-column {
        display: flex;
        flex-direction: column;
        gap: 2rem;
        width: 60%;
    }

    .left-inner-top {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: auto;
        height: 35%;
        align-content: stretch;
    }

    .left-inner-top-inner-column 
    {
        display: flex;
        flex-direction: column;
        width: 45%;
        height: 100%;
    }

    .left-inner-bottom {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
        align-content: stretch;
    }

    .right-column {
        display: flex;
        flex-direction: column;
        width: 40%;
        justify-content: space-between;
    }
</style>