<script>
	import Text from '$lib/Components/UI/text.svelte';
</script>

<div class="px-[16px] lg:px-[96px]">
	<div class="flex h-fit w-full flex-row lg:mt-[64px]">
		<div class=" flex w-full lg:w-1/2">
			<div class="flex flex-col">
				<Text type={'h1'}>Möglichkeiten als eingeschränkter Nutzer</Text>
				<Text type={'p'} classes={'w-full lg:w-3/4'}
					>Für Menschen, die das Internet täglich ohne Einschränkungen nutzen können, ist es
					selbstverständlich geworden, sich frei im Web zu bewegen. Doch während einige lediglich
					über schlechte oder veraltete Webseiten klagen, stellen diese für Anwender mit
					Einschränkungen echte Hindernisse dar. Hier sind drei Lösungsansätze, um diese Barrieren
					zu überwinden.</Text
				>
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
					>Screenreader: Inhalte hörbar machen</Text
				>
				<Text type={'p'} classes={'w-full'}
					>Screenreader sind eine essenzielle Software für Menschen mit Sehschwäche oder Blindheit.
					Sie lesen die Inhalte einer Website laut vor und ermöglichen somit eine barrierefreie
					Nutzung des Internets.</Text
				>
			</div>
		</div>
		<div class=" max-w-[469px] rounded-md border-[2px] border-gray-200 p-4">
			<div class="flex flex-col">
				<Text type={'h2'} classes={'text-[18px] font-[600] lg:text-[22px]'}
					>Vergrößerungssoftware: Texte und Details erkennen</Text
				>
				<Text type={'p'} classes={'w-full'}
					>Vergrößerungssoftware ist eine hilfreiche Lösung für Nutzer mit Sehschwäche. Sie
					ermöglicht es, Texte und Details auf dem Bildschirm zu vergrößern, um eine bessere
					Lesbarkeit zu gewährleisten.</Text
				>
			</div>
		</div>
		<div class="max-w-[469px] rounded-md border-[2px] border-gray-200 p-4">
			<div class="flex flex-col">
				<div>
					<Text type={'h2'} classes={'text-[18px] font-[600] lg:text-[22px]'}
						>Tastaturbedienung: Navigation ohne Maus</Text
					>
					<Text type={'p'} classes={'w-full'}
						>Die Tastaturnavigation ist eine effektive Methode für Nutzer mit motorischen
						Beeinträchtigungen oder anderen Einschränkungen. Sie erlaubt es, das Internet allein mit
						der Tastatur zu navigieren und somit eine barrierefreie Nutzung zu gewährleisten.</Text
					>
				</div>
			</div>
		</div>
	</div>
</div>
