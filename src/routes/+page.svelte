<script>
	import { goto } from '$app/navigation';
</script>

<div class="mt-[64px] flex w-full flex-row px-[96px]">
	<div class=" flex basis-1/2">
		<div class="flex flex-col">
			<h2 class="font-['Inter'] text-[24px] font-[500] text-black">Barrierefreiheit im Web:</h2>
			<h1 class="font-['Inter'] text-[32px] font-[700] text-black">
				Möglichkeiten als Nutzer und Entwickler
			</h1>
			<p class="w-3/4 font-['Inter'] text-[16px] font-[400] text-black">
				Eine Arbeit zu den Möglichkeiten der Barrierefreiheit im Internet, welche sich intensiv mit
				der Umsetzung einer barrierefreien Website beschäftigt. Sie entstand als Praxis- und
				Selbstanteil einer Facharbeit.
			</p>
			<button
				on:click={() => {
					goto('/facharbeit');
				}}
				aria-label="zur Facharbeitsseite"
				class="mt-4 w-fit cursor-pointer rounded-full bg-[#E8E8E8] px-[16px] py-[8px]"
			>
				<span class="font-['Inter'] text-[16px] font-[500] text-black">mehr Informationen</span>
			</button>
		</div>
	</div>
	<div class="flex basis-1/2 justify-end">
		<img src="man-with-laptop.svg" class="h-1/2 w-fit" alt="" />
	</div>
</div>
