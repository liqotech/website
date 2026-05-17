<script lang="ts">
	import NamespaceScheme from './architecture/network/NamespaceScheme.svelte';
	import NetworkScheme from './architecture/network/NetworkScheme.svelte';
	import OffloadingScheme from './architecture/network/OffloadingScheme.svelte';

	let title: HTMLElement;
</script>

<div
	id="features"
	class="c-min-h-screen flex h-screen flex-col items-center justify-center gap-8 overflow-hidden px-4"
>
	<h1
		bind:this={title}
		class="text-center text-xl font-black sm:text-2xl md:text-3xl lg:text-4xl xl:text-5xl"
	>
		Extend namespaces across clusters
	</h1>
	<NamespaceScheme customClass="w-full max-w-xl" />
	<div class="w-full max-w-2xl text-center text-lg font-medium text-gray-300 md:text-xl">
		Extend the namespaces of the consumer clusters, to have
		<span class="text-accent">namespaces distributed across the clusters</span>
		where resources are replicated. Allowing to <span class="text-accent">distribute Configurations, Secrets, Services</span> and other
		resources across your clusters.
	</div>
</div>
<div
	class="c-min-h-screen flex h-screen flex-col items-center justify-center gap-8 overflow-hidden px-4"
>
	<h1 class="text-center text-xl font-black sm:text-2xl md:text-3xl lg:text-4xl xl:text-5xl">
		Inter-cluster networking
	</h1>
	<NetworkScheme customClass="w-full max-w-xl" />
	<div class="w-full max-w-2xl text-center text-lg font-medium text-gray-300 md:text-xl">
		Create a seamless, <span class="text-accent">CNI and K8s distribution agnostic</span> <span class="text-accent"
			>network mesh between clusters</span
		>, enabling <span class="text-accent">direct communication</span> between pods of different clusters.
	</div>
</div>
<div
	class="c-min-h-screen flex h-screen flex-col items-center justify-center gap-8 overflow-hidden px-4"
>
	<h1
		bind:this={title}
		class="text-center text-xl font-black sm:text-2xl md:text-3xl lg:text-4xl xl:text-5xl"
	>
		Seemless pods offloading
	</h1>
	<OffloadingScheme customClass="w-full max-w-xl" />
	<div class="w-full max-w-2xl text-center text-lg font-medium text-gray-300 md:text-xl">
		Your consumer clusters can
		<span class="text-accent">transparently schedule pods on other clusters</span>. Enabling <span class="text-accent">resource
		sharing</span>, <span class="text-accent">data locality</span> or <span class="text-accent">geographical distribution</span> of the applications.
	</div>
</div>
