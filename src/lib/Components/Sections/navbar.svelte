<script lang="ts">
	import { goto } from '$app/navigation';
	import Text from '../UI/text.svelte';
	import { onDestroy } from 'svelte';
	import { scaleStore } from '$lib/stores';

	let navMenu = false; //false

	let isScaled: boolean;
	const unsubscribe = scaleStore.subscribe((value) => {
		isScaled = value;
	});

	function scaleText() {
		scaleStore.update((isScaled) => !isScaled);
	}

	onDestroy(() => {
		unsubscribe();
	});
</script>

<div class="hidden lg:block">
	<nav class="flex items-center justify-between bg-white px-[16px] pt-[8px] lg:px-[96px]">
		<button
			aria-label="zur Startseite"
			on:click={() => {
				goto('/');
			}}
		>
			<Text type={'h2'}>Barrierefreiheit im Web</Text>
		</button>

		<div class="flex gap-x-[64px]">
			<Text type={'a'} label={'zur Nutzer Seite'} goto={'/nutzer'}>Nutzer</Text>
			<Text type={'a'} label={'zur Entwickler Seite'} goto={'/entwickler'}>Entwickler</Text>
			<Text type={'a'} label={'zur Facharbeits Seite'} goto={'/facharbeit'}>Facharbeit</Text>
		</div>

		<button
			aria-label="Text vergrößern/ verkleinern"
			on:click={scaleText}
			class="align-center h-[43px] w-fit cursor-pointer rounded-[8px] bg-black px-4 text-center"
		>
			<Text type={'p'} size={'text-[14px]'} color={'text-white'}
				>Text {#if isScaled}
					verkleinern
				{:else}
					vergrößern
				{/if}</Text
			>
		</button>
	</nav>
</div>

<div class="block lg:hidden">
	<div class="relative z-50 mb-6 bg-white py-4">
		<div class="relative z-10 flex items-center justify-between px-[16px]">
			<Text type={'h2'}>Barrierefreiheit im Web</Text>
			<button
				aria-label={navMenu ? 'Menü schließen' : 'Menü öffnen'}
				class="material-icons"
				on:click={() => {
					navMenu = !navMenu;
				}}
			>
				{#if navMenu}
					expand_less
				{:else}
					menu
				{/if}</button
			>
		</div>
		{#if navMenu}
			<div class="fixed z-0 -mt-[2px] flex w-full flex-col gap-y-2 bg-white px-8 py-4 shadow-2xl">
				<Text type={'a'} label={'zur Nutzer Seite'} goto={'/nutzer'}>Nutzer</Text>
				<Text type={'a'} label={'zur Entwickler Seite'} goto={'/entwickler'}>Entwickler</Text>
				<Text type={'a'} label={'zur Facharbeits Seite'} goto={'/facharbeit'}>Facharbeit</Text>
				<button
					aria-label="Text vergrößern/ verkleinern"
					on:click={scaleText}
					class="mt-8 w-full cursor-pointer rounded-[8px] bg-black px-4 py-2 text-center align-middle"
				>
					<Text type={'p'} size={'text-[16px]'} color={'text-white'}
						>Text {#if isScaled}
							verkleinern
						{:else}
							vergrößern
						{/if}</Text
					>
				</button>
			</div>
		{/if}
	</div>
</div>
