<script lang="ts">
    export let type = '';
    export let color = 'bg-[#000000]';
    </script>
    
    {#if type == 'rect'}
    <!--Button Medium Rect Primary-->
        <button class="h-[43px] rounded-[8px] w-full {color} cursor-pointer px-4"><slot></slot></button>
    
    {:else if type == 'square'}
        <!--Button Medium Square Secondary-->
        <button class="h-[43px] w-[43px] rounded-[8px] {color} cursor-pointer"><slot></slot></button>
    
    {:else if type == 'circle'}
        <!--Button Medium circle Secondary-->
        <button class="h-[43px] w-[43px] rounded-full {color} cursor-pointer"><slot></slot></button>
    
    {:else if type == 'pill'}
        <!--Button Medium pill Secondary-->
        <button class="py-[14px] px-[16px] w-fit rounded-full {color} cursor-pointer"><slot></slot></button>
    {/if}
    
    