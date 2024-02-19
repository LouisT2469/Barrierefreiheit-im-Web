<script>
	import '../app.pcss';
	import Navbar from '$lib/Components/Sections/navbar.svelte';
	import Footer from '$lib/Components/Sections/footer.svelte';
</script>

<title>Barrierefreiheit im Web • LouisT2469</title>
<header>
	<Navbar />
</header>
<slot />
<Footer />
