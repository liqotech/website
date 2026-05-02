<script lang="ts">
	let { forcedClass = '' }: { forcedClass?: string } = $props();
</script>

<svg
	viewBox="0 0 24 24"
	aria-hidden="true"
	stroke="currentColor"
	class={forcedClass || 'inline-block h-6 w-6 stroke-current'}
>
	<path
		stroke-linecap="round"
		stroke-linejoin="round"
		d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
	/>
</svg>
