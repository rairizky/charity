<script>
	import Home from './pages/Home.svelte';
	import About from './pages/About.svelte';
	import Contact from './pages/Contact.svelte';

	import router from 'page';

	let page;
	router('/', () => (page = Home));
	router('/about', () => (page = About));
	router('/contact', () => (page = Contact));

	router.start();
</script>

<svelte:component this={page} />