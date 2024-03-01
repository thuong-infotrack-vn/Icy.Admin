<script>
	import '../app.pcss';
	import '../app.pcss';
	import Header from './Header.svelte';
	import './styles.css';
	import { BottomNav, BottomNavItem } from 'flowbite-svelte';
	import { IconHeart } from '@tabler/icons-svelte';
  import { page } from '$app/stores';
  $: activeUrl = $page.url.pathname;
</script>

<div class="app">
	<Header></Header>

	<main>
		<slot />
	</main>

	<BottomNav {activeUrl} position="absolute" classInner="grid-cols-4">
		<BottomNavItem btnName="Home" href="/">
			<IconHeart />
		</BottomNavItem>
		<BottomNavItem btnName="Quickstart" href="/docs/pages/quickstart" exact={false}>
			<IconHeart />
		</BottomNavItem>
		<BottomNavItem btnName="BottomNav" href="/docs/components/bottom-navigation">
			<IconHeart />
		</BottomNavItem>
		<BottomNavItem btnName="Accordion" href="/docs/components/accordion">
			<IconHeart />
		</BottomNavItem>
	</BottomNav>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
