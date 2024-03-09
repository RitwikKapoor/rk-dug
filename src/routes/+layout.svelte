<script>
	import '../app.pcss';
	import Navbar from '$lib/Navbar.svelte';
</script>

<div class="container mx-auto">
	<Navbar />
	<div class="pt-[123px]">
		<slot />
	</div>
</div>
