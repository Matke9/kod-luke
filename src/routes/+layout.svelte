<script lang="ts">
	import Nav from '$lib/components/Nav.svelte';
	import '../app.css';

	let { children } = $props();
</script>

<Nav></Nav>
<div class="px-20">
	{@render children()}
</div>
