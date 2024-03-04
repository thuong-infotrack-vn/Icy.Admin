<script>
	import '../app.pcss';
	import '../app.pcss';
	import Header from './Header.svelte';
	import './styles.css';
	import { BottomNav, BottomNavItem, NavBrand, Navbar, Tooltip,Button  } from 'flowbite-svelte';
	import { IconChartHistogram, IconHeart, IconHome, IconPlus, IconSettings, IconUsers } from '@tabler/icons-svelte';
  import { page } from '$app/stores';
  $: activeUrl = $page.url.pathname;
</script>

	<main>
		<Navbar rounded color="primary">
			<NavBrand href="/">
				<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Icy</span>
			</NavBrand>
			<div class="flex md:order-2">
				<Button size="sm">Ghi</Button>
			</div>
		</Navbar>
		<slot />
		<BottomNav position="absolute" classOuter="bottom-0 w-full rounded-none" navType="application" classInner="grid-cols-5">
			<BottomNavItem btnName="Trang chủ" appBtnPosition="left">
				<IconHome class="w-5 h-5 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-primary-600 dark:group-hover:text-primary-500" />
				<Tooltip arrow={false}>Trang chủ</Tooltip>
			</BottomNavItem>
			<BottomNavItem btnName="Khách hàng" appBtnPosition="middle">
				<IconUsers class="w-5 h-5 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-primary-600 dark:group-hover:text-primary-500" />
				<Tooltip arrow={false}>Khách hàng</Tooltip>
			</BottomNavItem>
			<div class="flex items-center justify-center">
				<BottomNavItem btnName="Ghi đá" appBtnPosition="middle" btnClass="inline-flex items-center justify-center w-10 h-10 font-medium bg-primary-600 rounded-full hover:bg-primary-700 group focus:ring-4 focus:ring-primary-300 focus:outline-none dark:focus:ring-primary-800">
					<IconPlus class="text-white" />
					<Tooltip arrow={false}>Ghi đá</Tooltip>
				</BottomNavItem>
			</div>
			<BottomNavItem btnName="Thống kê" appBtnPosition="middle">
				<IconChartHistogram class="w-5 h-5 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-primary-600 dark:group-hover:text-primary-500" />
				<Tooltip arrow={false}>Thống kê</Tooltip>
			</BottomNavItem>
			<BottomNavItem btnName="Cài đặt" appBtnPosition="right">
				<IconSettings class="w-5 h-5 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-primary-600 dark:group-hover:text-primary-500" />
				<Tooltip arrow={false}>Cài đặt</Tooltip>
			</BottomNavItem>
		</BottomNav>
</main>
