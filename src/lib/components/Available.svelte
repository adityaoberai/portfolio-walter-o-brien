<script>
	import { Typography, Button } from '@appwrite.io/pink-svelte';
	import { IconLinkedin, IconGithub } from '@appwrite.io/pink-icons-svelte';

	let linkedIn = 'https://www.linkedin.com/company/appwrite';
	let github = 'https://github.com/appwrite/appwrite';
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
		<Button.Anchor variant="secondary" size="medium" href={linkedIn}>
			<IconLinkedin />
			LinkedIn
		</Button.Anchor>
		<Button.Anchor variant="secondary" size="medium" href={github}>
			<IconGithub />
			GitHub
		</Button.Anchor>
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
