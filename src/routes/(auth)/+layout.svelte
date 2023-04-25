<script>
	import '../../app.css';
	import { page } from '$app/stores';
	import NavUl from '$lib/components/NavUl.svelte';
	import NavLi from '$lib/components/NavLi.svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import MyComp from '$lib/components/MyComp.svelte';
</script>

<Navbar>
	<NavUl>
		<NavLi data="home in navbar" href="/" active={$page.route.id === '/(auth)'}>Home (active:{$page.route.id === '/(auth)'})</NavLi>
		<NavLi data="about in navbar" href="/about" active={$page.route.id === '/(auth)/about'}>About (active:{$page.route.id === '/(auth)/about'})</NavLi>
	</NavUl>
</Navbar>

<MyComp>
	<NavUl>
		<NavLi data="home in mycomp" href="/" active={$page.route.id === '/(auth)'}>home (active:{$page.route.id === '/(auth)'})</NavLi>
		<NavLi data="about in mycomp" href="/about" active={$page.route.id === '/(auth)/about'}>about (active:{$page.route.id === '/(auth)/about'})</NavLi>
	</NavUl>
</MyComp>

<slot />
