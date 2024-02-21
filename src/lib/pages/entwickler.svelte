<script>
	import Text from '$lib/Components/UI/text.svelte';
</script>

<div class="px-[16px] lg:px-[96px]">
	<div class="flex h-fit w-full flex-row lg:mt-[64px]">
		<div class=" flex w-full lg:w-1/2">
			<div class="flex flex-col">
				<Text type={'h1'}>Möglichkeiten als Entwickler</Text>
				<Text type={'p'} classes={'w-full lg:w-3/4'}
					>Entwickler spielen eine entscheidende Rolle bei der Schaffung barrierefreier Webseiten.
					Es ist ihre Aufgabe, die Barrieren zu beseitigen und sicherzustellen, dass die Seiten den
					festgelegten Normen und Regeln entsprechen. Erfahren Sie, wie Entwickler die
					Barrierefreiheit vorantreiben können.</Text
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
					>Einhaltung von Regeln und Normen</Text
				>
				<Text type={'p'} classes={'w-full'}
					>Die Umsetzung barrierefreier Webseiten ist nicht nur ethisch, sondern auch gesetzlich
					vorgeschrieben. WCAG und BITV 2.0 sind wichtige Richtlinien, an denen sich Entwickler
					orientieren können bzw. in Behörden müssen, um die Zugänglichkeit sicherzustellen.</Text
				>
			</div>
		</div>
		<div class=" max-w-[469px] rounded-md border-[2px] border-gray-200 p-4">
			<div class="flex flex-col">
				<Text type={'h2'} classes={'text-[18px] font-[600] lg:text-[22px]'}
					>Barrierefreies Design für alle Nutzer</Text
				>
				<Text type={'p'} classes={'w-full'}
					>Barrierefreies Design ist von Vorteil für alle Nutzer, nicht nur für Menschen mit
					Einschränkungen. Aspekte wie starkes Kontrastverhältnis und responsive Design verbessern
					die Nutzererfahrung für jeden. Aber auch Buttons für Vergrößerung und Kontrast sind
					Möglichkeiten.</Text
				>
			</div>
		</div>
		<div class="max-w-[469px] rounded-md border-[2px] border-gray-200 p-4">
			<div class="flex flex-col">
				<div>
					<Text type={'h2'} classes={'text-[18px] font-[600] lg:text-[22px]'}
						>Optimierung der Seitenstruktur</Text
					>
					<Text type={'p'} classes={'w-full'}
						>Eine klare und organisierte Seitenstruktur, sowohl visuell als auch im Quelltext, ist
						entscheidend für die Barrierefreiheit. Die richtige Verwendung von HTML-Elementen und
						eine lineare Quelltextstruktur erleichtern die Nutzung von Screenreadern und verbessern
						die Zugänglichkeit.</Text
					>
				</div>
			</div>
		</div>
	</div>
</div>
