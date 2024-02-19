<script lang="ts">
export let type: string = '';
export let color: string = 'bg-[#000000]';
export let clickhandler: () => void;
</script>

{#if type == 'rect'}
<!--Button Medium Rect Primary-->
    <button on:click={clickhandler} class="h-[46px] rounded-[8px] w-full {color} cursor-pointer px-4"><slot></slot></button>

{:else if type == 'square'}
    <!--Button Medium Square Secondary-->
    <button on:click={clickhandler} class="h-[46px] w-[46px] rounded-[8px] {color} cursor-pointer"><slot></slot></button>

{:else if type == 'circle'}
    <!--Button Medium circle Secondary-->
    <button on:click={clickhandler} class="h-[46px] w-[46px] rounded-full {color} cursor-pointer"><slot></slot></button>

{:else if type == 'pill'}
    <!--Button Medium pill Secondary-->
    <button on:click={clickhandler} class="py-[14px] px-[16px] w-fit rounded-full {color} cursor-pointer"><slot></slot></button>
{/if}

