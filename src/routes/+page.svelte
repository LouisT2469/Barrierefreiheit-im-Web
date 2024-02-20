<script>
	import Navbar from '$lib/Components/Sections/navbar.svelte';
	import Footer from '$lib/Components/Sections/footer.svelte';
	import Home from '$lib/pages/home.svelte';
</script>

<div class="flex h-screen flex-col">
	<div class="sticky top-0 z-50"><Navbar /></div>
	<div class="grow"><Home /></div>
	<div class="static pb-4"><Footer /></div>
</div>
