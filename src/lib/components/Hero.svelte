<script>
	import ConnectivityIllustration from '$lib/components/ConnectivityIllustration.svelte';
</script>

<div class="mt-[-80px] c-min-h-screen flex h-screen flex-col items-center justify-center overflow-hidden">
	<div class="relative mt-4 h-[450px] w-full max-w-2xl mx-auto">
		<ConnectivityIllustration />
	</div>

	<div class="mx-4 flex flex-col items-center justify-center">
		<h1 class="c-text-gray-gradient my-4 text-6xl font-bold">Liqo</h1>
		<p class="text-center text-lg font-medium text-gray-300 md:text-xl">
			Enable <span class="text-accent">dynamic</span> and
			<span class="text-accent">transparent</span> Kubernetes multi-cluster topologies
		</p>
		<a
			class="btn btn-lg btn-primary my-8"
			href="https://docs.liqo.io/en/stable/examples/quick-start.html"
		>
			Get started
		</a>
	</div>
</div>
