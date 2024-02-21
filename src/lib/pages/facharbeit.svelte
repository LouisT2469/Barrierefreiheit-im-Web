<script lang="ts">
	import Text from '$lib/Components/UI/text.svelte';

	function downloadPDF() {
		const pdf = 'facharbeit.pdf';
		const link = document.createElement('a');
		link.href = pdf;
		link.download = 'barrierefreiheit_im_web.pdf';
		document.body.appendChild(link);
		link.click();
		document.body.removeChild(link);
	}
</script>

<div class="px-[16px] lg:px-[96px]">
	<div class="flex h-fit w-full flex-row lg:mt-[64px]">
		<div class=" flex w-full lg:w-1/2">
			<div class="flex flex-col">
				<Text type={'h1'}>Eine Facharbeit</Text>
				<Text type={'p'} classes={'w-full lg:w-3/4'}
					>Barrierefreiheit ist ein immer wichtiger werdendes Thema in unserer Gesellschaft,
					besonders in einer zunehmend digitalisierten Welt. In meiner Facharbeit befasste ich mich
					intensiv mit den Möglichkeiten für Nutzer und Entwickler, um Barrieren in der Webnutzung
					zu überwinden. <br /> <br /> Mein Ziel war es, die Bedeutung dieses Themas hervorzuheben, zudem
					wollte ich mich selber weiterbilden. Das Ergebnis meiner Arbeit ist diese Website, mit welcher
					ich den Mehraufwand einer barrierefreien Website bewerten wollte.</Text
				>
			</div>
		</div>
		<div class="flex w-0 justify-end lg:w-1/2">
			<img src="man-with-laptop.svg" class="h-64 w-fit md:block" alt="Mann der am Laptop sitzt." />
		</div>
	</div>

	<!--part 2-->
	<div class="my-[16px] mb-8 flex flex-wrap justify-between gap-y-4 lg:my-[80px]">
		<div class="rounded-md border-[2px] border-gray-200 p-4 lg:max-w-[40%]">
			<div class="flex flex-col justify-between">
				<Text type={'h2'} classes={'text-[18px] font-[600] lg:text-[22px]'}
					>Download der Facharbeit
				</Text>
				<Text type={'p'} classes={'w-full mb-[16px]'}
					>Interessierte Personen können die Arbeit hier herunterladen und mehr über die Bedeutung
					und Umsetzung von Barrierefreiheit erfahren.</Text
				>
				<form on:submit|preventDefault={downloadPDF}>
					<div>
						<label for="checkbox" class="mb-[12px] flex cursor-pointer">
							<input
								id="checkbox"
								type="checkbox"
								required
								class="form-checkbox mt-[3.5px] h-[18px] w-[18px] appearance-none text-black ring-0 focus:ring-0"
							/>
							<Text type={'p'} classes={'ml-[8px] italic'}
								>Ich akzeptiere, dass diese Facharbeit ausschließlich zu privaten Zwecken genutzt
								werden darf.</Text
							>
						</label>

						<button
							type="submit"
							aria-label="Facharbeit herunterladen"
							title="Herunterladen"
							class="rounded-full bg-[#E8E8E8] px-[16px] py-[10px]"
						>
							<Text type={'p'} classes={'text-[14px] font-medium'}>Herunterladen</Text>
						</button>
					</div>
				</form>
			</div>
		</div>
	</div>
</div>
