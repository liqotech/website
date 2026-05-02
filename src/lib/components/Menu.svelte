<script>
	import Github from './Icons/Github.svelte';
	import Slack from './Icons/Slack.svelte';
</script>

<ul class="menu md:menu-horizontal font-medium max-md:h-full max-md:w-full">
	<li>
		<a href="#features">Features</a>
	</li>
	<li>
		<a href="#use-cases">Use Cases</a>
	</li>
	<li>
		<a href="#adopters">Adopters</a>
	</li>
	<li>
		<a href="https://docs.liqo.io" target="_blank" rel="noopener noreferrer">Docs</a>
	</li>
	<li>
		<a href="https://liqo-io.slack.com/join/shared_invite/zt-h20212gg-g24YvN6MKiD9bacFeqZttQ" target="_blank" rel="noopener noreferrer" aria-label="Slack">
			<Slack forcedClass="h-5 w-5 fill-base-content" />
		</a>
	</li>
	<li>
		<a href="https://github.com/liqotech/liqo" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
			<Github forcedClass="h-6 w-6 fill-base-content" />
		</a>
	</li>
</ul>
