<script>
	import Text from '$lib/Components/UI/text.svelte';
	import { goto } from '$app/navigation';
</script>

<div class="px-[16px] lg:px-[96px]">
	<div class="flex h-fit w-full flex-row lg:mt-[64px]">
		<div class=" flex w-full lg:w-1/2">
			<div class="flex flex-col">
				<Text type={'h1'}>Kontaktmöglichkeiten</Text>
				<Text type={'p'} classes={'w-full lg:w-3/4'}
					>Ihre Meinungen und Erfahrungen zu meiner Facharbeit sind mir wichtig! Falls Sie Fragen
					oder Anmerkungen haben oder gerne mehr über meine Re­cher­chen erfahren möchten, stehe ich
					Ihnen gerne zur Verfügung.
				</Text>
				<button
					on:click={() => {
						window.location.href = 'mailto:facharbeit@louist2469.de';
					}}
					aria-label="Email-Verknüpfung"
					class="mt-4 w-fit cursor-pointer rounded-full bg-[#E8E8E8] px-[16px] py-[8px]"
				>
					<Text type={'p'} weight={'font-[500]'}>facharbeit@louist2469.de</Text>
				</button>
			</div>
		</div>
		<div class="flex w-0 justify-end lg:w-1/2">
			<img src="man-with-laptop.svg" class="h-64 w-fit md:block" alt="Mann der am Laptop sitzt." />
		</div>
	</div>
</div>
