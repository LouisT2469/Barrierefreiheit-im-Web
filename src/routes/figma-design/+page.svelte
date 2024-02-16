<!-- Redirect.svelte -->
<script>
    import { onMount } from 'svelte';
  
    const targetDomain = 'https://www.figma.com/file/z0jlq6G54HjmksSoxv9sKf/Facharbeit-V1?type=design&node-id=0%3A1&mode=design&t=iNtcAEqUezvCkX3u-1';
  
    onMount(() => {
      window.location.href = targetDomain;
    });
  </script>
  
  <svelte:head>
    <title>Weiterleitung</title>
    <meta http-equiv="refresh" content="0;url={targetDomain}" />
  </svelte:head>
  
  <noscript>
    <meta http-equiv="refresh" content="0;url={targetDomain}" />
    <p>Bitte klicken Sie <a href="{targetDomain}">hier</a>, um weitergeleitet zu werden.</p>
  </noscript>
  
  <p>Bitte warten Sie, während Sie zu {targetDomain} weitergeleitet werden...</p>
  