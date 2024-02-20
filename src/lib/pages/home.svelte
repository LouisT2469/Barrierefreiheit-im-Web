<script>
	import { goto } from '$app/navigation';
</script>

<div class="px-[16px] lg:px-[96px]">
	<div class="flex h-fit w-full flex-row lg:mt-[64px]">
		<div class=" flex w-full lg:w-1/2">
			<div class="flex flex-col">
				<h2 class="font-['Inter'] text-[18px] font-[600] text-black lg:text-[24px]">
					Barrierefreiheit im Web:
				</h2>
				<h1 class="font-['Inter'] text-[26px] font-[700] text-black lg:text-[32px]">
					Möglichkeiten als Nutzer und Entwickler
				</h1>
				<p class="w-full font-['Inter'] text-[16px] font-[400] text-black lg:w-3/4">
					Eine Arbeit zu den Möglichkeiten der Barrierefreiheit im Internet, welche sich intensiv
					mit der Umsetzung einer barrierefreien Website beschäftigt. Sie entstand als Praxis- und
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
		<div class="flex w-0 justify-end lg:w-1/2">
			<img src="man-with-laptop.svg" class="h-64 w-fit md:block" alt="Mann der am Laptop sitzt." />
		</div>
	</div>

	<!--part 2-->
	<div class="my-[16px] mb-8 flex flex-wrap justify-between gap-y-4 lg:my-[80px]">
		<div class="max-w-[469px] rounded-md border-[2px] border-gray-200 p-4">
			<div class="flex flex-col justify-between">
				<h2 class="font-['Inter'] text-[18px] font-[600] text-black lg:text-[24px]">
					Was ist Barrierefreiheit?
				</h2>
				<p class="w-full font-['Inter'] text-[16px] font-[400] text-black">
					Erfahren Sie, was Barrierefreiheit im Internet wirklich bedeutet. Es geht nicht nur um die
					erleichterte Nutzung von Websites für körperlich eingeschränkte Personen, sondern um jede
					Form von Einschränkung, sei es durch Alter...
				</p>
				<div class="mt-6 flex justify-between">
					<button
						on:click={() => {
							goto('/entwickler');
						}}
						aria-label="zur Nutzerseite"
						class="h-[46px] w-fit cursor-pointer rounded-full bg-[#E8E8E8] px-[16px] py-[8px]"
					>
						<span class="font-['Inter'] text-[16px] font-[500] text-black">mehr Informationen</span>
					</button>
				</div>
			</div>
		</div>
		<div class=" max-w-[469px] rounded-md border-[2px] border-gray-200 p-4">
			<div class="flex flex-col">
				<h2 class="font-['Inter'] text-[18px] font-[600] text-black lg:text-[24px]">
					Möglichkeiten als Nutzer:
				</h2>
				<p class="w-full font-['Inter'] text-[16px] font-[400] text-black">
					Erfahren Sie hier, wie Sie mit spezieller Software und Hardware das Internet barrierefrei
					nutzen können. Entdecken Sie ausgewählte IT-Lösungen, die es Ihnen ermöglichen, das
					Internet ohne Einschränkungen zu erkunden und zu nutzen.
				</p>
				<div class="mt-6 flex justify-between">
					<button
						on:click={() => {
							goto('/nutzer');
						}}
						aria-label="zur Nutzerseite"
						class="h-[46px] w-fit cursor-pointer rounded-full bg-[#E8E8E8] px-[16px] py-[8px]"
					>
						<span class=" font-['Inter'] text-[16px] font-[500] text-black">mehr Informationen</span
						>
					</button>
				</div>
			</div>
		</div>
		<div class="max-w-[469px] rounded-md border-[2px] border-gray-200 p-4">
			<div class="flex flex-col">
				<div>
					<h2 class="font-['Inter'] text-[18px] font-[600] text-black lg:text-[24px]">
						Möglichkeiten als Entwickler:
					</h2>
					<p class="w-full font-['Inter'] text-[16px] font-[400] text-black">
						Viele IT-Lösungen dienen lediglich als Ergänzung und funktionieren nur dann, wenn
						Entwickler sich an bestimmte Normen und Regeln halten. Erfahren Sie hier ausgewählte
						Ansätze und Techniken zur Förderung...
					</p>
				</div>
				<div class="mt-6 flex h-full justify-between">
					<button
						on:click={() => {
							goto('/entwickler');
						}}
						aria-label="zur Nutzerseite"
						class="h-[46px] w-fit cursor-pointer rounded-full bg-[#E8E8E8] px-[16px] py-[8px]"
					>
						<span class="font-['Inter'] text-[16px] font-[500] text-black">mehr Informationen</span>
					</button>
				</div>
			</div>
		</div>
	</div>
</div>
