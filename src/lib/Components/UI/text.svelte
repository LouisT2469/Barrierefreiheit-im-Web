<script lang="ts">
	import { onMount } from 'svelte';
	import { onDestroy } from 'svelte';
	import { scaleStore } from '$lib/stores';

	export let type = '';

	export let size = 'text-[16px]';

	export let weight = 'font-[400]';

	export let color = 'text-black';
	export let goto = '/';

	export let label = '';
	export let classes = '';

	let isScaled: boolean;
	const unsubscribe = scaleStore.subscribe((value) => {
		isScaled = value;
	});

	onDestroy(() => {
		unsubscribe();
	});
</script>

{#if type == 'p'}
	<p
		class="break-words {weight} {color} {classes} {isScaled ? 'text-[32px]' : size}"
	>
		<slot />
	</p>
{:else if type == 'h1'}
	<h1
		class="break-words font-[700] {color} {classes} {isScaled
			? 'text-[52px] lg:text-[64px]'
			: 'text-[26px] lg:text-[32px]'}"
	>
		<slot />
	</h1>
{:else if type == 'h2'}
	{#if isScaled}
		<h2
			class="break-words {classes.length == 0
				? 'font-[700]'
				: ''}  {color} {classes} text-[40px]"
		>
			<slot />
		</h2>
	{:else}
		<h2
			class="break-words {classes.length == 0
				? 'text-[20px] font-[700]'
				: ''}  {color} {classes}"
		>
			<slot />
		</h2>
	{/if}
{:else if type == 'a'}
	<a
		class="break-words font-[500] {color} {classes} {isScaled
			? 'text-[32px]'
			: size}"
		aria-label={label}
		href={goto}><slot /></a
	>
{/if}
