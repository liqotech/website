<script>
	import Drawer from './Icons/Drawer.svelte';
	import Menu from './Menu.svelte';
</script>

<div class="mx-auto h-20 max-w-[90rem] px-4 py-4">
	<div class="flex justify-between">
		<div>
			<!-- Logo -->
			<label
				for="main-menu"
				aria-label="open sidebar"
				class="btn btn-square btn-ghost inline-flex md:hidden"
			>
				<Drawer />
			</label>
		</div>
		<div class="hidden md:block">
			<Menu />
		</div>
	</div>
</div>
