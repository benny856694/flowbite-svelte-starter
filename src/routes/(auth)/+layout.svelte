<script>
	import '../../app.css';
	import { Navbar } from 'flowbite-svelte';
	import { page } from '$app/stores';
	import NavUl from '../../lib/components/NavUl.svelte';
	import NavLi from '../../lib/components/NavLi.svelte';
	let darkmodebtn =
		'text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 focus:outline-none focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 rounded-lg text-lg p-2.5 fixed right-4 top-2 z-50';
</script>

<Navbar let:hidden let:toggle>
	<NavUl {hidden}>
		<NavLi href="/" active={$page.route.id === '/(auth)'}>Home</NavLi>
		<NavLi href="/about" active={$page.route.id === '/(auth)/about'}>About</NavLi>
	</NavUl>
</Navbar>

<div>
	<NavUl>
		<NavLi href="/" active={$page.route.id === '/(auth)'}>home active: {$page.route.id === '/(auth)'}</NavLi>
		<NavLi href="/about" active={$page.route.id === '/(auth)/about'}>about active: {$page.route.id === '/(auth)/about'}</NavLi>
	</NavUl>
</div>

<slot />
