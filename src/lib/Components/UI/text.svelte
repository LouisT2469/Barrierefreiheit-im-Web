<script lang="ts">
	export let type = 'normal';

	export let size = 'text-[16px]';

	export let weight = 'font-[600]';

	export let color = 'text-black';
    export let goto = '/';
</script>

{#if (type == 'h1')}
	<!--Heading 1-->
	<h1 class="text-[28px] font-[700] font-['Inter'] {color}"><slot /></h1>
{:else if (type == 'h2')}
	<!--Heading 2-->
	<h2 class="text-[20px] font-[700] font-['Inter'] {color}"><slot /></h2>
{:else if (type == 'custom')}
	<!--Custom Text-->
	<p class="{size} font-['Inter'] {weight} {color}"><slot /></p>
{:else if (type == 'navbar')}
<a class="text-[16px] font-['Inter'] font-[500] {color}" href="{goto}"><slot/></a>
{:else}
	<!--Normal text-->
	<p class="text-[16px] font-[400] font-['Inter'] {color}"><slot /></p>
{/if}
