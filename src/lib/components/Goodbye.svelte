<script lang="ts">
	import { onMount } from 'svelte';
	import { cubicOut } from 'svelte/easing';
	import { Tween } from 'svelte/motion';

	let scale = new Tween(2, { duration: 1000, easing: cubicOut });
	let opacity = new Tween(0, { duration: 1000, easing: cubicOut });
	let text: HTMLHeadingElement;

	onMount(() => {
		const maxScroll = text.offsetTop;
		const handleScroll = () => {
			const scrollY = window.scrollY;
			const progress = Math.min(scrollY / maxScroll, 1);

			scale.set(2 - progress); // Scale down from 2 to 1
			opacity.set(progress); // Increase opacity from 0 to 1
		};
		handleScroll(); // Call it once to set initial state
		window.addEventListener('scroll', handleScroll);

		return () => {
			window.removeEventListener('scroll', handleScroll);
		};
	});
</script>

<div class="c-min-h-screen flex items-center justify-center overflow-hidden px-8">
	<h1
		bind:this={text}
		class="sm:leading-5xl sticky top-0 flex h-screen w-screen items-center justify-center text-center text-3xl font-black sm:text-4xl md:text-6xl lg:text-7xl"
		style="transform: scale({scale.current}); opacity: {opacity.current};"
	>
		Say goodbye to complex integrations 👋
	</h1>
</div>
