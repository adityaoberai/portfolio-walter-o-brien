<script>
	import { Typography, Button } from '@appwrite.io/pink-svelte';

	const projects = [
		{
			title: 'ScenGen',
			description: 'AI-powered scenario generation engine used in cybersecurity and healthcare'
		},
		{
			title: 'Risk Management Platform',
			description: 'Risk assessment tool created for financial and defense industries'
		},
		{
			title: 'ConciergeUp Intelligence-as-a-Service',
			description: 'Service offering personalized technical and strategic solutions'
		}
	];
</script>

<section id="projects" class="container">
	<Typography.Title size="medium">Projects</Typography.Title>
	<div class="project-cards">
		{#each projects as project}
			<Button.Button variant="secondary" size="medium">
				<div class="card">
					<Typography.Title size="small">
						{project.title}
					</Typography.Title>
					<Typography.Text variant="l-400">
						{project.description}
					</Typography.Text>
				</div>
			</Button.Button>
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
		gap: 1rem;
		overflow: hidden;
		align-items: start;
	}
</style>
