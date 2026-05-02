<script lang="ts">
	import Icon from '@iconify/svelte';

	const highlights = [
		{
			icon: 'noto:airplane',
			title: 'Workload Offloading',
			description:
				'<span class="font-semibold">Seamless workload offloading</span> to remote clusters. Collapse an entire remote cluster to a <span class="font-semibold">virtual node</span>, fully compliant with standard Kubernetes.',
		},
		{
			icon: 'noto:left-right-arrow',
			title: 'Inter-cluster Networking',
			description:
				'Transparent multi-cluster <span class="font-semibold">pod-to-pod</span> and <span class="font-semibold">pod-to-service</span> connectivity regardless of CNI plugins. All cross-cluster traffic flows through <span class="font-semibold">secured tunnels</span>.',
		},
		{
			icon: 'noto:floppy-disk',
			title: 'Cross-cluster Storage',
			description:
				'Remote execution of <span class="font-semibold">stateful workloads</span> with the data gravity approach. Extend <span class="font-semibold">database HA</span> techniques to multi-cluster scenarios seamlessly.',
		},
		{
			icon: 'noto:puzzle-piece',
			title: 'Extensibility',
			description:
				'<span class="font-semibold">Modular and extensible</span> architecture designed to integrate with existing tools and platforms. Build on top of Liqo to fit your <span class="font-semibold">specific multi-cluster requirements</span>.',
		},
		{
			icon: 'noto:page-with-curl',
			title: 'Declarative Configuration',
			description:
				'Fully <span class="font-semibold">cloud-native</span> and declarative. Manage multi-cluster topologies <span class="font-semibold">as code</span>, seamlessly integrating with <span class="font-semibold">GitOps workflows</span>, CI/CD pipelines, and automation tools.',
		},
		{
			icon: 'noto:cloud',
			title: 'Multi-environment Support',
			description:
				'Works across <span class="font-semibold">heterogeneous infrastructures</span>: on-premise, public cloud, edge, and multi-cloud. Supports <span class="font-semibold">any Kubernetes distribution</span>, managed or self-hosted, with <span class="font-semibold">no vendor lock-in</span>.',
		},
	];
</script>

<section class="mx-auto max-w-[90rem] px-8 py-24">
	<div class="mb-24 text-center">
		<h2 class="text-3xl font-black sm:text-4xl md:text-5xl">
			Why <span class="text-primary">Liqo</span>?
		</h2>
		<p class="mx-auto mt-8 max-w-2xl text-lg font-medium opacity-70">
			A complete toolkit for <span class="text-accent">Kubernetes multi-cluster</span>, from networking to storage, designed to be <span class="text-accent">declarative</span>, <span class="text-accent">extensible</span>, and <span class="text-accent">production-ready</span>.
		</p>
	</div>
	<div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
		{#each highlights as item}
			<div class="card card-border bg-base-100 border-base-300">
				<div class="card-body">
					<div class="text-4xl">
						<Icon icon={item.icon} />
					</div>
					<h3 class="card-title mt-2">{item.title}</h3>
					<p class="opacity-70">{@html item.description}</p>
				</div>
			</div>
		{/each}
	</div>
</section>
