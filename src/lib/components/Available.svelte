<script>
	import { Typography, Button } from '@appwrite.io/pink-svelte';
	import { IconLinkedin, IconGithub } from '@appwrite.io/pink-icons-svelte';
</script>

<section id="available" class="container">
	<div class="content">
		<Typography.Title size="medium">
			<span>●</span>
			Available for new projects
		</Typography.Title>

		<Typography.Text variant="l-500"
			>Available for new partnerships and collaborations. Let's chat!</Typography.Text
		>
	</div>

	<div class="social-buttons">
		<Button.Button variant="secondary" size="medium">
			<IconLinkedin />
			LinkedIn
		</Button.Button>
		<Button.Button variant="secondary" size="medium">
			<IconGithub />
			GitHub
		</Button.Button>
	</div>
</section>

<style>
	#available {
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	.content {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	span {
		color: var(--color-bgcolor-success);
	}

	.social-buttons {
		display: flex;
		flex-direction: column;
		width: 100%;
		gap: 0.5rem;
	}
</style>
