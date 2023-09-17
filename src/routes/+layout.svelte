<script lang="ts">
	import '../app.postcss';

	import { AppShell } from '@skeletonlabs/skeleton';
	import { AppBar } from '@skeletonlabs/skeleton';
	import { LightSwitch } from '@skeletonlabs/skeleton';
	import { Drawer, getDrawerStore } from '@skeletonlabs/skeleton';
	import type { DrawerSettings, DrawerStore } from '@skeletonlabs/skeleton';
	import Navigation from '$lib/Navigation.svelte';
	import { initializeStores } from '@skeletonlabs/skeleton';
	import PageTransition from './transition.svelte';

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
	
	export let data;

</script>

<Drawer>
	<a href="/" on:click={drawerClose}>
		<header>
			<div class="flex items-center justify-center mx-auto">
			<img src="/images/Logo_2.webp" class="hidden dark:block max-h-16 w-fit p-2" alt="SS Logo" />
			<img src="/images/Logodark_2.webp" class="block dark:hidden max-h-16 w-fit p-2" alt="SS Logo" />
			
				<span class=" text-2xl font-extrabold uppercase p-4 bg-gradient-to-br from-gray-800 to-gray-400 bg-clip-text text-transparent box-decoration-clone">Sanele Shange</span>
			</div>
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
	<a href="/">

		<div class="flex items-center justify-center mx-auto">

			
			<img src="/images/Logo_2.webp" class="hidden dark:block max-h-16 w-fit px-2" alt="SS Logo" />
			<img src="/images/Logodark_2.webp" class="block dark:hidden max-h-16 w-fit px-2" alt="SS Logo" />
			<span class="place-self-center text-4xl md:text-6xl font-extrabold uppercase bg-gradient-to-br from-gray-800 dark:from-gray-200 to-gray-400 dark:to-gray-500 bg-clip-text text-transparent box-decoration-clone"> Sanele Shange</span>
		</div>
	</a>
	
		
	
	<svelte:fragment slot="trail"><LightSwitch /></svelte:fragment>
</AppBar>


	</svelte:fragment>
	
	<!-- (sidebarRight) -->
	<!-- (pageHeader) -->
	<!-- Router Slot -->
	<PageTransition url={data.url}>
	<slot />
</PageTransition>
	<!-- ---- / ---- -->
	<svelte:fragment slot="pageFooter">
	
	
	
<footer class="m-2">
    <div class="w-full mx-auto max-w-screen-xl p-2 md:flex md:items-center md:justify-between text-center">
      <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400 hover:underline font-medium">Driven by Performance. #BreakingLimits
    </span>
  
    </div>
</footer>




	</svelte:fragment>
	<!-- (footer) -->
</AppShell>