<script>
    import '../app.css';
    import { Root } from '@appwrite.io/pink-svelte';
    import { ThemeDark } from '$lib/themes';
    import { browser } from '$app/environment';
</script>
{#if browser}
<Root theme={ThemeDark}>
    <slot />
</Root>
{/if}