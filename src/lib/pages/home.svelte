<script>
	import { goto } from '$app/navigation';
	import Text from '$lib/Components/UI/text.svelte';
</script>

<div class="px-[16px] lg:px-[96px]">
	<div class="flex h-fit w-full flex-row lg:mt-[64px]">
		<div class=" flex w-full lg:w-1/2">
			<div class="flex flex-col">
				<Text type={'h2'} classes={'text-[18px] font-[600] lg:text-[24px]'}
					>Barrierefreiheit im Web:</Text
				>
				<Text type={'h1'}>Möglichkeiten als Nutzer und Entwickler</Text>
				<Text type={'p'} classes={'w-full lg:w-3/4'}
					>Eine Arbeit zu den Möglichkeiten der Barrierefreiheit im Internet, welche sich intensiv
					mit der Umsetzung einer barrierefreien Website beschäftigt. Sie entstand als Praxis- und
					Selbstanteil einer Facharbeit.</Text
				>
				<button
					on:click={() => {
						goto('/facharbeit');
					}}
					aria-label="zur Facharbeitsseite"
					class="mt-4 w-fit cursor-pointer rounded-full bg-[#E8E8E8] px-[16px] py-[8px]"
				>
					<Text type={'p'} weight={'font-[500]'}>mehr Informationen</Text>
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
				<Text type={'h2'} classes={'text-[18px] font-[600] lg:text-[22px]'}
					>Was ist Barrierefreiheit?</Text
				>
				<Text type={'p'} classes={'w-full'}
					>Barrierefreiheit im Internet bedeutet nicht nur einfache Nutzung für körperlich
					eingeschränkte Personen, sondern auch für alle anderen, wie Ältere oder Nutzer mit
					unterschiedlichen Geräten. Web-Entwicklung zielt darauf ab, Websites trotz vieler
					Einschränkungen möglichst zugänglich zu machen, obwohl 100%ige Barrierefreiheit utopisch
					ist.</Text
				>
			</div>
		</div>
		<div class=" max-w-[469px] rounded-md border-[2px] border-gray-200 p-4">
			<div class="flex flex-col">
				<Text type={'h2'} classes={'text-[18px] font-[600] lg:text-[22px]'}
					>Möglichkeiten als Nutzer:</Text
				>
				<Text type={'p'} classes={'w-full'}
					>Erfahren Sie hier, wie Sie mit spezieller Software und Hardware das Internet barrierefrei
					nutzen können. Entdecken Sie ausgewählte IT-Lösungen, die es Ihnen ermöglichen, das
					Internet ohne Einschränkungen zu erkunden und zu nutzen.</Text
				>
				<div class="mt-6 flex justify-between">
					<button
						on:click={() => {
							goto('/nutzer');
						}}
						aria-label="zur Nutzerseite"
						class="h-[46px] w-fit cursor-pointer rounded-full bg-[#E8E8E8] px-[16px] py-[8px]"
					>
						<Text type={'p'} weight={'font-[500]'}>mehr Informationen</Text>
					</button>
				</div>
			</div>
		</div>
		<div class="max-w-[469px] rounded-md border-[2px] border-gray-200 p-4">
			<div class="flex flex-col">
				<div>
					<Text type={'h2'} classes={'text-[18px] font-[600] lg:text-[22px]'}
						>Möglichkeiten als Entwickler:</Text
					>
					<Text type={'p'} classes={'w-full'}
						>Viele IT-Lösungen dienen lediglich als Ergänzung und funktionieren nur dann, wenn
						Entwickler sich an bestimmte Normen und Regeln halten. Erfahren Sie hier ausgewählte
						Ansätze und Techniken zur Förderung von Barrierefreiheit.</Text
					>
				</div>
				<div class="mt-6 flex h-full justify-between">
					<button
						on:click={() => {
							goto('/entwickler');
						}}
						aria-label="zur Nutzerseite"
						class="h-[46px] w-fit cursor-pointer rounded-full bg-[#E8E8E8] px-[16px] py-[8px]"
					>
						<Text type={'p'} weight={'font-[500]'}>mehr Informationen</Text>
					</button>
				</div>
			</div>
		</div>
	</div>
</div>
