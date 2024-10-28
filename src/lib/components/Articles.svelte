<script>
	import { Typography, Button } from '@appwrite.io/pink-svelte';

	const articles = [
		{
			title: 'The Role of AI in Modern Security Solutions',
			url: 'https://appwrite.io/blog'
		},
		{
			title: 'High-Stakes Problem Solving: Lessons from Scorpion',
			url: 'https://appwrite.io/blog'
		},
		{
			title: 'How Scenario Generation Can Predict Outcomes',
			url: 'https://appwrite.io/blog'
		}
	];
</script>

<section id="articles" class="container">
	<Typography.Title size="medium">Articles</Typography.Title>
	<div class="article-cards">
		{#each articles as article}
			<Button.Anchor variant="secondary" size="medium" href={article.url}>
				<div class="card">
					<Typography.Title size="small">
						{article.title}
					</Typography.Title>
				</div>
			</Button.Anchor>
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
