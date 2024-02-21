<script lang="ts">
	export let type = 'normal';

	export let size = 'text-[16px]';

	export let weight = 'font-[400]';

	export let color = 'text-black';
	export let goto = '/';

	export let label = '';
	export let classes = '';
</script>


{#if type == 'p'}
	<p class="font-['Inter'] {size} {weight} {color} {classes}">
		<slot />
	</p>
{:else if type == 'h1'}
	<h1 class="font-['Inter'] text-[26px] font-[700] {color} {classes} lg:text-[32px]">
		<slot />
	</h1>{:else if type == 'h2'}
	<h2
		class="font-['Inter'] {classes.length == 0 ? 'text-[20px] font-[700]' : ''}  {color} {classes}"
	>
		<slot />
	</h2>
{:else if type == 'a'}
	<a class="font-['Inter'] {size} font-[500] {color} {classes}" aria-label={label} href={goto}
		><slot /></a
	>
{/if}
