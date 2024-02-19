<script>
	import { goto } from '$app/navigation';
</script>

<nav class="mt-[8px] flex items-center justify-between px-[96px]">
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
