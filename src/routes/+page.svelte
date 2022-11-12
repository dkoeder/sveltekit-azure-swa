<script context="module">
	export const prerender = true;

	export async function load({ fetch }) {
		const response = await fetch('/api/alive');

		return {
			status: response.status,
			props: {
				status: response.ok && (await response.json())
			}
		};
	}
</script>

<script>
	export let status;
</script>

<pre>{JSON.stringify(status, null, 2)}</pre>
<h1>Welcome to SvelteKit - Azure static web app - changed paths</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>


<!-- for azure functions -->
<!-- https://github.com/geoffrich/svelte-adapter-azure-swa -->
 <!-- https://github.com/tguelcan/sveltekit-azure/blob/master/src/routes/index.svelte -->

 <!-- https://github.com/saimon24/sveltekit-stream -->
