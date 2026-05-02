<script lang="ts">
	import Icon from '@iconify/svelte';
	const useCases = [
		{
			icon: 'noto:robot',
			title: 'AI Inference at Scale',
			description:
				'Serve AI models across clusters by transparently accessing <span class="font-semibold">remote GPUs</span>. Schedule inference workloads on <span class="font-semibold">GPU-equipped provider clusters</span> without changing your deployments.',
			tags: ['GPU', 'AI/ML'],
		},
		{
			icon: 'noto:brain',
			title: 'Distributed ML Training',
			description:
				'Burst <span class="font-semibold">training jobs</span> to clusters with available GPU capacity. Leverage Liqo\'s network fabric for <span class="font-semibold">high-throughput cross-cluster communication</span> during distributed training.',
			tags: ['GPU', 'AI/ML'],
		},
		{
			icon: 'noto:chart-increasing',
			title: 'Cloud Bursting',
			description:
				'Seamlessly <span class="font-semibold">offload peak workloads</span> from on-premise clusters to cloud providers. Scale beyond your <span class="font-semibold">local capacity</span> without re-architecting applications.',
			tags: ['Hybrid Cloud'],
		},
		{
			icon: 'noto:globe-showing-europe-africa',
			title: 'Edge Computing',
			description:
				'Run your <span class="font-semibold">workloads at the edge</span> while centrally managing deployments and configurations.',
			tags: ['Edge', 'AI/ML'],
		},
		{
			icon: 'noto:clockwise-vertical-arrows',
			title: 'High Availability',
			description:
				'Extend <span class="font-semibold">stateful workloads across regions</span>. Achieve <span class="font-semibold">multi-cluster HA</span> without managing independent replicas manually.',
			tags: ['HA'],
		},
		{
			icon: 'noto:cloud',
			title: 'Hybrid & Multi-Cloud',
			description:
				'Span workloads across <span class="font-semibold">on-premise, public cloud, and multi-cloud</span> environments. A <span class="font-semibold">single control plane</span> with Liqo\'s virtual nodes abstracts away infrastructure differences.',
			tags: ['Hybrid Cloud'],
		},
	];
</script>

<section id="use-cases" class="mx-auto max-w-[90rem] px-8 py-24">
	<div class="mb-24 text-center">
		<h2 class="text-3xl font-black sm:text-4xl md:text-5xl">
			Use Cases
		</h2>
		<p class="mx-auto mt-8 max-w-2xl text-lg font-medium opacity-70">
			From <span class="text-accent">AI workloads</span> requiring remote GPU access to <span class="text-accent">hybrid cloud</span> deployments and <span class="text-accent">edge computing</span>: Liqo adapts to your multi-cluster needs.
		</p>
	</div>
	<div class="mt-16 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
		{#each useCases as useCase}
			<div class="card card-border bg-base-100 border-base-300">
				<div class="card-body">
					<div class="text-4xl">
						<Icon icon={useCase.icon} />
					</div>
					<h3 class="card-title mt-2">{useCase.title}</h3>
					<p class="opacity-70">{@html useCase.description}</p>
					<div class="card-actions mt-4">
						{#each useCase.tags as tag}
							<span class="badge badge-soft badge-primary badge-sm">{tag}</span>
						{/each}
					</div>
				</div>
			</div>
		{/each}
	</div>
</section>
