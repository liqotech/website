<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';
	import Menu from '$lib/components/Menu.svelte';
	import TopBanner from '$lib/components/TopBanner.svelte';
	import '../app.css';
	import '../custom.css';
	let { children } = $props();
</script>

<div class="drawer">
	<input id="main-menu" type="checkbox" class="drawer-toggle" />
	<div class="drawer-content">
		<TopBanner
			link=""
		>
			<!-- Announcements go here! -->
		</TopBanner>
		<Header />
		{@render children()}
		<Footer />
	</div>
	<div class="drawer-side z-10">
		<label for="main-menu" aria-label="close sidebar" class="drawer-overlay"></label>
		<div class="menu bg-base-200 text-base-content min-h-full w-80 p-4">
			<Menu />
		</div>
	</div>
</div>
