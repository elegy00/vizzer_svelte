<script>
	export let name;

	import Renderer from './Renderer.svelte';
	import Device from './Device.svelte';

</script>
 
<style>
	h1 {
		color: purple; 
	}
</style>

<h1>Hello {name}!</h1> 
<Renderer/>
<Device/>
