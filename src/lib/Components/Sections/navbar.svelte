<script>
	import { goto } from '$app/navigation';
	let navMenu = false; //false
</script>

<div class="hidden lg:block">
	<nav class="mt-[8px] flex items-center justify-between px-[16px] lg:px-[96px]">
		<h2 class="font-['Inter'] text-[20px] font-[700] text-black">Barrierefreiheit im Web</h2>

		<div class="flex gap-x-[64px]">
			<a
				class="font-['Inter'] text-[16px] font-[500] text-black"
				aria-label="zur Entwickler Seite"
				href="/entwickler">Entwickler</a
			>
			<a
				class="font-['Inter'] text-[16px] font-[500] text-black"
				aria-label="zur Nutzer Seite"
				href="/nutzer">Nutzer</a
			>
			<a
				class="font-['Inter'] text-[16px] font-[500] text-black"
				aria-label="zur Facharbeitsseite"
				href="/facharbeit">Facharbeit</a
			>
		</div>

		<button
			aria-label="zur Newsletter Seite"
			on:click={() => {
				goto('/newsletter');
			}}
			class="h-[43px] w-fit cursor-pointer rounded-[8px] bg-black px-4"
		>
			<span class="font-['Inter'] text-[14px] text-white">Newsletter</span>
		</button>
	</nav>
</div>

<div class="block lg:hidden">
	<div class="relative z-50 mb-6 bg-white py-4">
		<div class="relative z-10 flex items-center justify-between px-[16px]">
			<h2 class="font-['Inter'] text-[20px] font-[700] text-black">Barrierefreiheit im Web</h2>
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
				<a
					class=" font-['Inter'] text-[16px] font-[500] text-black"
					aria-label="zur Entwickler Seite"
					href="/entwickler">Entwickler</a
				>
				<a
					class="rounded-md font-['Inter'] text-[16px] font-[500] text-black"
					aria-label="zur Nutzer Seite"
					href="/nutzer">Nutzer</a
				>
				<a
					class="rounded-md font-['Inter'] text-[16px] font-[500] text-black"
					aria-label="zur Facharbeitsseite"
					href="/facharbeit">Facharbeit</a
				>
				<button
					aria-label="zur Newsletter Seite"
					on:click={() => {
						goto('/newsletter');
					}}
					class="mt-8 h-[43px] w-full cursor-pointer rounded-[8px] bg-black px-4"
				>
					<span class="font-['Inter'] text-[16px] text-white">Newsletter</span>
				</button>
			</div>
		{/if}
	</div>
</div>
