<script>
	import { Typography } from '@appwrite.io/pink-svelte';

	const skills = [
		'Artificial Intelligence (AI)',
		'Machine Learning (ML)',
		'Cybersecurity',
		'Cryptography',
		'Network Engineering'
	];
</script>

<section id="skills" class="container">
	<Typography.Title size="medium">Skills</Typography.Title>
	<div class="skills-badges">
		{#each skills as skill}
			<div class="badge">
				<Typography.Text variant="l-500">
					{skill}
				</Typography.Text>
			</div>
		{/each}
	</div>
</section>

<style>
	.skills-badges {
		display: flex;
		flex-direction: row;
		gap: 1rem;
		flex-wrap: wrap;
	}

	.skills-badges > .badge {
		border: 0.125rem solid var(--color-border-neutral-strong);
		background-color: var(--color-bgcolor-neutral-default);
		border-radius: 0.5rem;
		padding: 0.25rem 1rem;
	}
</style>
