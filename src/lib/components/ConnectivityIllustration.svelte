<script lang="ts">
	import Logo from '$lib/components/Logo.svelte';

	let { customClass = '', style = '' }: { customClass?: string; style?: string } = $props();

	const nodes = [
		{ x: 115, y: 80, r: 6 },
		{ x: 490, y: 70, r: 5 },
		{ x: 65, y: 260, r: 7 },
		{ x: 535, y: 245, r: 5 },
		{ x: 150, y: 390, r: 6 },
		{ x: 450, y: 380, r: 7 }
	];

	const center = { x: 300, y: 225 };
</script>

<div class="relative h-full w-full {customClass}" {style}>
	<!-- Background glow -->
	<div class="absolute inset-0 flex items-center justify-center">
		<div class="bg-primary h-56 w-56 rounded-full opacity-15 blur-3xl"></div>
	</div>

	<!-- Ripple waves emanating from center -->
	<div class="absolute inset-0 flex items-center justify-center pointer-events-none">
		<div class="ripple border-primary"></div>
		<div class="ripple border-primary" style="animation-delay: 2s"></div>
		<div class="ripple border-primary" style="animation-delay: 4s"></div>
	</div>

	<!-- Network constellation SVG -->
	<svg
		class="absolute inset-0 h-full w-full text-primary"
		viewBox="0 0 600 450"
		fill="none"
		aria-hidden="true"
	>
		<!-- Orbit rings -->
		<circle
			cx={center.x} cy={center.y} r="105"
			stroke="#fff" stroke-opacity="0.12" stroke-width="1"
			stroke-dasharray="4 8"
		/>
		<circle
			cx={center.x} cy={center.y} r="170"
			stroke="#fff" stroke-opacity="0.08" stroke-width="1"
			stroke-dasharray="3 10"
		/>
		<circle
			cx={center.x} cy={center.y} r="240"
			stroke="#fff" stroke-opacity="0.04" stroke-width="1"
			stroke-dasharray="2 12"
		/>

		<!-- Connection lines with flowing data effect -->
		{#each nodes as node, i}
			<line
				x1={center.x} y1={center.y}
				x2={node.x} y2={node.y}
				stroke="#fff" stroke-opacity="0.12"
				stroke-width="1" stroke-dasharray="6 4"
				class="connection-line"
				style="animation-delay: {i * 0.3}s"
			/>
		{/each}

		<!-- Small intermediary dots for richer network feel -->
		<circle cx="205" cy="150" r="2" fill="currentColor" fill-opacity="0.2" />
		<circle cx="395" cy="145" r="1.5" fill="currentColor" fill-opacity="0.15" />
		<circle cx="180" cy="245" r="1.5" fill="currentColor" fill-opacity="0.2" />
		<circle cx="420" cy="235" r="2" fill="currentColor" fill-opacity="0.15" />
		<circle cx="225" cy="310" r="1.5" fill="currentColor" fill-opacity="0.18" />
		<circle cx="375" cy="305" r="2" fill="currentColor" fill-opacity="0.15" />
		<circle cx="300" cy="120" r="1.5" fill="currentColor" fill-opacity="0.12" />
		<circle cx="300" cy="340" r="1.5" fill="currentColor" fill-opacity="0.12" />

		<!-- Cluster node pulse rings -->
		{#each nodes as node, i}
			<circle
				cx={node.x} cy={node.y} r={node.r + 10}
				stroke="currentColor" fill="none"
				class="node-pulse"
				style="animation-delay: {i * 0.5}s"
			/>
		{/each}

		<!-- Cluster node circles -->
		{#each nodes as node, i}
			<circle
				cx={node.x} cy={node.y} r={node.r}
				fill="currentColor"
				class="node-dot"
				style="animation-delay: {i * 0.4}s"
			/>
		{/each}
	</svg>

	<!-- Central Logo -->
	<div class="absolute inset-0 flex items-center justify-center">
		<Logo customClass="h-32 drop-shadow-[0_0_30px_rgba(50,108,229,0.3)]" />
	</div>
</div>

<style>
	.ripple {
		position: absolute;
		width: 60px;
		height: 60px;
		border-radius: 50%;
		border-width: 1px;
		border-style: solid;
		animation: ripple 6s ease-out infinite;
	}

	@keyframes ripple {
		0% {
			transform: scale(1);
			opacity: 0.15;
		}
		100% {
			transform: scale(8);
			opacity: 0;
		}
	}

	.connection-line {
		animation: dash 3s linear infinite;
	}

	@keyframes dash {
		to {
			stroke-dashoffset: -20;
		}
	}

	.node-pulse {
		transform-box: fill-box;
		transform-origin: center;
		animation: node-pulse 3s ease-out infinite;
	}

	@keyframes node-pulse {
		0% {
			transform: scale(1);
			stroke-opacity: 0.25;
		}
		100% {
			transform: scale(2.5);
			stroke-opacity: 0;
		}
	}

	.node-dot {
		animation: glow 4s ease-in-out infinite;
	}

	@keyframes glow {
		0%,
		100% {
			fill-opacity: 0.4;
		}
		50% {
			fill-opacity: 0.7;
		}
	}
</style>
