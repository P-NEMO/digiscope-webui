<script>
   let tabSet = 0
   import {TabGroup,Tab} from '@skeletonlabs/skeleton';

</script>

<TabGroup  justify="justify-center" hover="bg-purple-700" padding='px-40 py-5' spacing="space-y-2" class="mt-5">
	<Tab bind:group={tabSet} name="tab1" value={0}>Summary</Tab>
	<Tab bind:group={tabSet} name="tab2" value={1}>Clouds</Tab>
	<Tab bind:group={tabSet} name="tab3" value={2}>Wind</Tab>
	<!-- Tab Panels --->
	<svelte:fragment slot="panel">
		{#if tabSet === 0}
			(tab panel 1 contents)
		{:else if tabSet === 1}
			(tab panel 2 contents)
		{:else if tabSet === 2}
			(tab panel 3 contents)
		{/if}
	</svelte:fragment>
</TabGroup>