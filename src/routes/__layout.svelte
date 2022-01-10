<script>
	import 'materialize-css/dist/css/materialize.min.css';
import Footer from '../Components/Footer.svelte';
	import { onMount } from 'svelte';
	import Navbar from '../Components/Navbar.svelte';

	let MyComponent;

	onMount(async () => {
		const module = await import('materialize-css/dist/js/materialize.min.js');
		MyComponent = module.default;
		M.AutoInit();
	});
</script>

<Navbar />


<slot/>

<Footer />


<style>
	:global(*){
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}
</style>