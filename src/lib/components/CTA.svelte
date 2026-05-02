<script lang="ts">
	import Github from './Icons/Github.svelte';
	import Slack from './Icons/Slack.svelte';
</script>

<section class="bg-base-200 px-8 py-24">
	<div class="mx-auto max-w-3xl text-center">
		<h2 class="text-3xl font-black sm:text-4xl md:text-5xl">
			Ready to go <span class="text-primary">multi-cluster</span>?
		</h2>
		<p class="mt-8 text-lg font-medium opacity-70">
			Get started with Liqo in <span class="text-accent">minutes</span>. Install on your clusters, establish a peering, and start <span class="text-accent">offloading workloads</span>. No complex configurations required.
		</p>
		<div class="mt-10 flex flex-wrap items-center justify-center gap-4">
			<a
				class="btn btn-primary btn-lg"
				href="https://docs.liqo.io/en/stable/examples/quick-start.html"
				target="_blank"
				rel="noopener noreferrer"
			>
				Quick Start Guide
			</a>
			<a
				class="btn btn-outline btn-lg"
				href="https://github.com/liqotech/liqo"
				target="_blank"
				rel="noopener noreferrer"
			>
				<Github forcedClass="h-5 w-5 fill-current" />
				View on GitHub
			</a>
			<a
				class="btn btn-ghost btn-lg"
				href="https://liqo-io.slack.com/join/shared_invite/zt-h20212gg-g24YvN6MKiD9bacFeqZttQ"
				target="_blank"
				rel="noopener noreferrer"
			>
				<Slack forcedClass="h-5 w-5 fill-current" />
				Join Slack
			</a>
		</div>
		<div class="mockup-code mt-12 text-left bg-base-100">
			<pre data-prefix="$"><code>liqoctl peer --remote-kubeconfig remote-cluster.yaml</code></pre>
			<pre data-prefix="" class="text-success"><code>✓ Peering established successfully</code></pre>
		</div>
	</div>
</section>
