<script lang="ts">
	import Github from './Icons/Github.svelte';
	import X from './Icons/X.svelte';
	import Slack from './Icons/Slack.svelte';
	import YouTube from './Icons/YouTube.svelte';
	import Logo from './Logo.svelte';
</script>

<footer class="bg-base-200">
	<div class="footer footer-vertical sm:footer-horizontal mx-auto max-w-[90rem] px-8 py-10">
		<aside class="max-w-xs">
			<div class="flex items-center gap-3">
				<Logo customClass="h-8 w-8" />
				<span class="text-xl font-bold">Liqo</span>
			</div>
			<p class="mt-2 text-sm opacity-70">
				Enable dynamic and seamless Kubernetes multi-cluster topologies. Open source, Apache-2.0
				licensed.
			</p>
			<p class="mt-1 text-sm opacity-50">
				Born at Polytechnic of Turin, maintained with ❤️ by the Liqo community.
			</p>
		</aside>
		<nav>
			<h6 class="footer-title">Project</h6>
			<a href="https://docs.liqo.io" target="_blank" rel="noopener noreferrer" class="link link-hover">Documentation</a>
			<a href="https://docs.liqo.io/en/stable/examples/quick-start.html" target="_blank" rel="noopener noreferrer" class="link link-hover">Quick Start</a>
			<a href="https://github.com/liqotech/liqo/releases" target="_blank" rel="noopener noreferrer" class="link link-hover">Releases</a>
		</nav>
		<nav>
			<h6 class="footer-title">Community</h6>
			<a href="https://liqo-io.slack.com/join/shared_invite/zt-h20212gg-g24YvN6MKiD9bacFeqZttQ" target="_blank" rel="noopener noreferrer" class="link link-hover">Slack</a>
			<a href="https://github.com/liqotech/liqo-community" target="_blank" rel="noopener noreferrer" class="link link-hover">Community Repo</a>
			<a href="https://github.com/liqotech/liqo/blob/master/CONTRIBUTING.md" target="_blank" rel="noopener noreferrer" class="link link-hover">Contributing</a>
			<a href="https://github.com/liqotech/liqo/blob/master/ADOPTERS.md" target="_blank" rel="noopener noreferrer" class="link link-hover">Adopters</a>
		</nav>
		<nav>
			<h6 class="footer-title">Social</h6>
			<div class="flex gap-4">
				<a href="https://github.com/liqotech/liqo" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
					<Github forcedClass="h-6 w-6 fill-base-content opacity-70 hover:opacity-100 transition-opacity" />
				</a>
				<a href="https://liqo-io.slack.com/join/shared_invite/zt-h20212gg-g24YvN6MKiD9bacFeqZttQ" target="_blank" rel="noopener noreferrer" aria-label="Slack">
					<Slack forcedClass="h-6 w-6 fill-base-content opacity-70 hover:opacity-100 transition-opacity" />
				</a>
				<a href="https://x.com/liqo_io" target="_blank" rel="noopener noreferrer" aria-label="X / Twitter">
					<X forcedClass="h-6 w-6 fill-base-content opacity-70 hover:opacity-100 transition-opacity" />
				</a>
				<a href="https://www.youtube.com/channel/UCYbWJMfwy3P6xT4JI_K84xw" target="_blank" rel="noopener noreferrer" aria-label="YouTube">
					<YouTube forcedClass="h-6 w-6 fill-base-content opacity-70 hover:opacity-100 transition-opacity" />
				</a>
			</div>
		</nav>
	</div>
	<div class="border-base-300 border-t px-8 py-4">
		<div class="mx-auto flex max-w-[90rem] flex-col items-center justify-between gap-2 text-sm opacity-60 sm:flex-row">
			<p>© 2019-{new Date().getFullYear()} The Liqo Authors. Licensed under Apache-2.0.</p>
		</div>
	</div>
</footer>
