<script>
	import { Typography, Button } from '@appwrite.io/pink-svelte';

	const articles = [
		'The Role of AI in Modern Security Solutions',
		'High-Stakes Problem Solving: Lessons from Scorpion',
		'How Scenario Generation Can Predict Outcomes'
	];
</script>

<section id="articles" class="container">
	<Typography.Title size="medium">Articles</Typography.Title>
	<div class="article-cards">
		{#each articles as article}
			<Button.Button variant="secondary" size="medium">
				<div class="card">
					<Typography.Title size="small">
						{article}
					</Typography.Title>
				</div>
			</Button.Button>
		{/each}
	</div>
</section>

<style>
	.article-cards {
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
