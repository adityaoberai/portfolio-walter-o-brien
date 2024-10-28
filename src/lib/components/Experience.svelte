<script>
	import { Typography } from '@appwrite.io/pink-svelte';

	const experiences = [
		{
			title: 'CEO',
			company: 'Scorpion Computer Services',
			date: '1998 — Present',
			description: [
				'Founded and grew Scorpion into a global consulting firm.',
				'Provides high-stakes problem-solving for Fortune 500 companies and government agencies.',
				'Develops AI-driven solutions for complex technology, security, and engineering challenges.'
			]
		},
		{
			title: 'Contributor',
			company: 'Think Tanks',
			date: '2010 — Present',
			description: [
				'Supports private and public sectors with high-level policy and strategy contributions.',
				'Advises on strengthening security measures and technological infrastructure for large organizations.'
			]
		},
		{
			title: 'Cybersecurity and Intelligence Advisor',
			company: 'Miscellaneous Projects',
			date: '2008 — Present',
			description: [
				'Advises on cybersecurity strategies for military and governmental entities.',
				'Protects sensitive data by developing advanced strategies to counteract cyber threats.'
			]
		}
	];
</script>

<section id="experience" class="container">
	<Typography.Title size="medium">Experience</Typography.Title>
	<div class="jobs">
		{#each experiences as { title, company, date, description }}
			<div class="job">
				<div class="time">
					<Typography.Text variant="m-500">
						{date}
					</Typography.Text>
				</div>
				<div class="info">
					<div class="info-text">
						<Typography.Title size="small">
							{company}
						</Typography.Title>
						<Typography.Text variant="m-500">
							{title}
						</Typography.Text>
					</div>
					<ul>
						{#each description as desc}
							<li>{desc}</li>
						{/each}
					</ul>
				</div>
			</div>
		{/each}
	</div>
</section>

<style>
	#experience {
		display: flex;
		flex-direction: column;
		justify-content: start;
	}

	.jobs {
		display: flex;
		flex-direction: column;
		gap: 1.5rem;
		width: 100%;
		justify-content: start;
		align-items: stretch;
		justify-items: stretch;
	}

	.job {
		display: flex;
		flex-direction: row;
		gap: 1rem;
		justify-content: space-between;
		margin-bottom: 0.5rem;
	}

	.time {
		width: 33.33%;
	}

	.info {
		display: flex;
		flex-direction: column;
		width: 66.67%;
		justify-content: start;
		gap: 0.75rem;
	}

	.info-text {
		display: flex;
		flex-direction: column;
		gap: 0.25rem;
	}

	ul {
		list-style-type: disc;
		padding-inline-start: 1rem;
	}

	@media (max-width: 768px) {
		.job {
			flex-direction: column;
			gap: 0.25rem;
		}

		.time {
			width: 100%;
		}

		.info {
			width: 100%;
		}
	}
</style>
