<script>
	import '@skeletonlabs/skeleton/themes/theme-gold-nouveau.css';
	import '@skeletonlabs/skeleton/styles/all.css';
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	// import { LightSwitch } from '@skeletonlabs/skeleton';
</script>

<svelte:head>
	<title>Twitch Raffle Logger</title>
</svelte:head>

<AppShell>
	<svelte:fragment slot="header">
		<AppBar>
			<svelte:fragment slot="lead">
				<a href="/">
					<strong class="text-3xl">Who won?</strong>
				</a>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<div class="input-group input-group-divider grid-cols-[auto_1fr_auto]">
					<button class="input-group-shim"><i class="fa-solid fa-search" /></button>
					<input type="search" placeholder="Twitch Username" />
					<!-- <button class="variant-filled-primary">Go</button> -->
				</div>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
