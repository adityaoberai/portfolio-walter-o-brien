<script>
	import { Typography } from "@appwrite.io/pink-svelte";

    const experiences = [
        {
            title: 'CEO',
            company: 'Scorpion Computer Services',
            date: '1998 - Present',
            description: [
                'Founded and grew Scorpion into a global consulting firm.',
                'Provides high-stakes problem-solving for Fortune 500 companies and government agencies.',
                'Develops AI-driven solutions for complex technology, security, and engineering challenges.'
            ]
        },
        {
            title: 'Contributor',
            company: 'Think Tanks',
            date: '2010 - Present',
            description: [
                'Supports private and public sectors with high-level policy and strategy contributions.',
                'Advises on strengthening security measures and technological infrastructure for large organizations.'
            ]
        },
        {
            title: 'Cybersecurity and Intelligence Advisor',
            company: 'Miscellaneous Projects',
            date: '2008 - Present',
            description: [
                'Advises on cybersecurity strategies for military and governmental entities.',
                'Protects sensitive data by developing advanced strategies to counteract cyber threats.'
            ]
        },
    ]
</script>

<section id="experience" class="container">
    <h3>
        <Typography.Title size="large">
            Experience
        </Typography.Title>
    </h3>
    <div class="jobs">
    {#each experiences as { title, company, date, description }}
        <div class="job">
            <div class="time">
                <Typography.Text variant="m-500">
                    {date}
                </Typography.Text>
            </div>
            <div class="info">
                <Typography.Title size="small">
                        {company}
                </Typography.Title>
                <p>
                    <Typography.Text variant="m-500">{title}</Typography.Text>
                </p>
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
        width: 100%;
        max-width: 100%;
    }

    .jobs {
        display: flex;
        flex-direction: column;
        gap: 2rem;
        width: 100%;
    }
    
    .job {
        display: flex;
        flex-direction: row;
        gap: 2rem;
        justify-content: space-between;
    }

    .time {
        max-width: 50%;
    }

    .info {
        max-width: 50%;
        justify-content: start;
    }

    ul {
        list-style-type: disc;
        padding-inline-start: 1rem;
    }
</style>