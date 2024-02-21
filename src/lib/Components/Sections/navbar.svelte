<script>
	import { goto } from '$app/navigation';
	import Text from '../UI/text.svelte';
	let navMenu = false; //false

	let scale = true;

	function scaleText() {
		scale = !scale;
		localStorage.setItem('scale', String(scale));
	}
</script>

<div class="hidden lg:block">
	<nav class="mt-[8px] flex items-center justify-between px-[16px] lg:px-[96px]">
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
			class="h-[43px] w-fit cursor-pointer rounded-[8px] bg-black px-4"
		>
			<Text type={'p'} size={'text-[14px]'} color={'text-white'}
				>Text {#if scale}
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
					class="mt-8 h-[43px] w-full cursor-pointer rounded-[8px] bg-black px-4"
				>
					<Text type={'p'} size={'text-[16px]'} color={'text-white'}
						>Text {#if scale}
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
