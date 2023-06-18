<script>
	import { Autocomplete } from '@skeletonlabs/skeleton';
	import { Stepper, Step } from '@skeletonlabs/skeleton';
	let inputTemp = '';

	import flavorOptions from "$lib/objects/nebula.json";

	function onFlavorSelection(event) {
		inputTemp = event.detail.label;
	}

</script>

<Stepper class='m-8 bg-black bg-opacity-40 p-8 rounded-lg shadow-gray-100'>
	<Step class="">
		<svelte:fragment slot="header">Select a cosmic body</svelte:fragment>
		<div class="card w-full max-w-sm max-h-48 p-4 overflow-y-auto" tabindex="-1">
			<input class="input" type="search" name="demo" bind:value={inputTemp} placeholder="Search..." />
			<Autocomplete bind:input={inputTemp} on:selection={onFlavorSelection} options={flavorOptions}  />
		</div>
		<br>
	</Step>
	<Step>
		<strong>Selected {inputTemp}</strong> 
		
		(content)
	</Step>
	<!-- ... -->
</Stepper>
			

