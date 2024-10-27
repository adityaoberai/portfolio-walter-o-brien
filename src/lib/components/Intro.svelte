<script>
    import { Avatar, Typography, Divider } from '@appwrite.io/pink-svelte';
    import Profile from '$lib/images/profile.webp';
</script>

<section id="intro">
    <div class="intro-content">
        <Avatar src={Profile} size="x-large" alt="ChatGPT-generated image of Walter O'Brien" />
        <div class="intro-content-text">
            <Typography.Title size="x-large">
                Walter O'Brien
            </Typography.Title>
            <Typography.Title size="large">
                Technology Entrepreneur
            </Typography.Title>
        </div>
    </div>
    <Divider />
</section>

<style>
    #intro {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        align-items: start;
        width: 100%;
    }

    .intro-content {
        display: flex;
        flex-direction: row;
        gap: 1rem;
        align-items: center;
        justify-content: center;
    }

    .intro-content-text {
        display: flex;
        flex-direction: column;
    }
</style>