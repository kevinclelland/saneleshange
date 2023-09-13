<script lang="ts">
	import '../app.postcss';

	import { AppShell } from '@skeletonlabs/skeleton';
	import { AppBar } from '@skeletonlabs/skeleton';
	import { LightSwitch } from '@skeletonlabs/skeleton';
	import { Drawer, getDrawerStore } from '@skeletonlabs/skeleton';
	import type { DrawerSettings, DrawerStore } from '@skeletonlabs/skeleton';
	import Navigation from '$lib/Navigation.svelte';
	import { initializeStores } from '@skeletonlabs/skeleton';

	initializeStores();

	const drawerStore = getDrawerStore();
	const drawerSettings: DrawerSettings = {
	
	bgDrawer: '',
	bgBackdrop: '',
	width: 'max-w-xs md:max-w-md',
	
	
};
function drawerOpen(): void {
		drawerStore.open(drawerSettings);
	}
	function drawerClose(): void {
		drawerStore.close();
	}
	

</script>

<Drawer>
	<a href="/" on:click={drawerClose}>
		<header>
			<h2 class="h2 p-2">Sanele Shange</h2>
		</header>
	</a>
		
			<hr />
	<Navigation />
</Drawer>

<!-- <AppShell>...</AppShell> -->

<AppShell>
	<svelte:fragment slot="header">
		
		
<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
	<svelte:fragment slot="lead">

	<div class="flex items-center">
        <button class="btn btn-sm mr-4" on:click={drawerOpen}>
            <span>
                <svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
                    <rect width="100" height="20" />
                    <rect y="30" width="100" height="20" />
                    <rect y="60" width="100" height="20" />
                </svg>
            </span>
        </button>
        
    </div>



	</svelte:fragment>
	<h1 class="h1 text-center">Sanele Shange</h1>
	<svelte:fragment slot="trail"><LightSwitch /></svelte:fragment>
</AppBar>


	</svelte:fragment>
	
	<!-- (sidebarRight) -->
	<!-- (pageHeader) -->
	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->
	<svelte:fragment slot="pageFooter">
	
	
	
<footer class="m-4">
    <div class="w-full mx-auto max-w-screen-xl p-4 md:flex md:items-center md:justify-between">
      <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">© 2023 <a href="https://saneleshange.com/" class="hover:underline">Sanele Shange</a>. Triathlete.
    </span>
    <ul class="flex flex-wrap items-center mt-3 text-sm font-medium text-gray-500 dark:text-gray-400 sm:mt-0">
        <li>
            <a href="#" class="mr-4 hover:underline md:mr-6 ">About</a>
        </li>
        <li>
            <a href="#" class="mr-4 hover:underline md:mr-6">Privacy Policy</a>
        </li>
        <li>
            <a href="#" class="mr-4 hover:underline md:mr-6">Licensing</a>
        </li>
        <li>
            <a href="#" class="hover:underline">Contact</a>
        </li>
    </ul>
    </div>
</footer>




	</svelte:fragment>
	<!-- (footer) -->
</AppShell>