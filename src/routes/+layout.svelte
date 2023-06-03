<script>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file

	import {AppShell} from '@skeletonlabs/skeleton';

	import Footer from '$lib/landing/Footer.svelte';
	import Header from '$lib/landing/Header.svelte';

	import Sidebar from '$lib/landing/Sidebar.svelte';

	const routes = [
        'guiding','camera','weather','fix','arts','stats','tools'
    ]

    const names = [
        'Guiding',"Camera","Weather","AstroFix Studio","AstroArts Studio","Hardware Stats","Tools"
    ]

</script>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header"> <Header /> </svelte:fragment>
	<svelte:fragment slot="pageHeader">Page Header</svelte:fragment>
	<svelte:fragment slot="sidebarLeft"><Sidebar routes={routes} names={names}/></svelte:fragment>
	<slot />
	<svelte:fragment slot="footer"> <Footer /></svelte:fragment>
</AppShell>
