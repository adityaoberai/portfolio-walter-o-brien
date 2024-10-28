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
		<div class="available-component">
			<Available />
		</div>
		<div class="about-component">
			<About />
		</div>
		<div class="experience-component">
			<Experience />
		</div>

		<div class="right-column">
			<div class="skills-component">
				<Skills />
			</div>
			<div class="projects-component">
				<Projects />
			</div>
			<div class="articles-component">
				<Articles />
			</div>
		</div>
	</div>
</main>

<style>
	main {
		width: 1440px;
		height: 100%;
		margin: auto;
	}

	.intro-content,
	.resume-content {
		width: 80%;
		height: 80%;
		margin: auto;
	}

	.intro-content {
		display: flex;
		flex-direction: row;
		height: max-content;
	}

	.resume-content {
		display: grid;
		grid-template-rows: 0.8fr 2.2fr;
		grid-template-columns: 1fr 1fr 1fr;
		row-gap: 1.25rem;
		column-gap: 1.25rem;
	}

	.available-component {
		grid-row: 1 / span 1;
		grid-column: 1 / span 1;
	}

	.about-component {
		grid-row: 1 / span 1;
		grid-column: 2 / span 1;
	}

	.experience-component {
		grid-row: 2 / span 2;
		grid-column: 1 / span 2;
	}

	.right-column {
		grid-row: 1 / span 3;
		grid-column: 3 / span 1;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		gap: 1rem;
	}

	@media (min-width: 1200px) and (max-width: 1440px) {
		main {
			width: 1200px;
		}
	}

	@media (min-width: 768px) and (max-width: 1200px) {
		main {
			width: 90%;
			padding: 2rem 0;
			height: fit-content;
		}

		.experience-component {
			height: min-content;
		}

		.right-column {
			justify-content: stretch;
		}
	}

	@media (max-width: 768px) {
		main {
			width: 90%;
			padding: 2rem 0;
		}

		.resume-content {
			display: flex;
			flex-direction: column;
			gap: 2rem;
			width: 100%;
		}

		.right-column {
			gap: 2rem;
		}
	}
</style>
