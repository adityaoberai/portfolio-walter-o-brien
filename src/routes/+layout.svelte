<script>
	import '../app.css';
	import 'the-new-css-reset/css/reset.css';
	import { Root } from '@appwrite.io/pink-svelte';
	import { ThemeDark } from '$lib/themes';
	import { browser } from '$app/environment';
</script>

{#if browser}
	<Root theme={ThemeDark}>
		<slot />
	</Root>
{/if}
