<script>
	import { Typography, Button } from '@appwrite.io/pink-svelte';

	const projects = [
		{
			title: 'ScenGen',
			description: 'AI-powered scenario generation engine used in cybersecurity and healthcare',
			url: 'https://github.com/appwrite/appwrite'
		},
		{
			title: 'Risk Management Platform',
			description: 'Risk assessment tool created for financial and defense industries',
			url: 'https://github.com/appwrite/appwrite'
		},
		{
			title: 'ConciergeUp Intelligence-as-a-Service',
			description: 'Service offering personalized technical and strategic solutions',
			url: 'https://github.com/appwrite/appwrite'
		}
	];
</script>

<section id="projects" class="container">
	<Typography.Title size="medium">Projects</Typography.Title>
	<div class="project-cards">
		{#each projects as project}
			<Button.Anchor variant="secondary" size="medium" href={project.url}>
				<div class="card">
					<Typography.Title size="small">
						{project.title}
					</Typography.Title>
					<Typography.Text variant="l-400">
						{project.description}
					</Typography.Text>
				</div>
			</Button.Anchor>
		{/each}
	</div>
</section>

<style>
	.project-cards {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		width: 100%;
	}

	.card {
		display: flex;
		flex-direction: column;
		width: 100%;
		gap: 0.5rem;
		overflow: hidden;
		align-items: start;
	}
</style>
