<script>
	import Foot from './Food.svelte';
	import Carru from './Carru.svelte';
	import Colllapse from './Colllapse.svelte';
    import Navegator from './navegator/Navegator.svelte';
	import { Button , Dropdown , DropdownItem , DropdownDivider , Chevron } from 'flowbite-svelte'
	import { DarkMode } from 'flowbite-svelte';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Input } from 'flowbite-svelte'
	
	const items = new Array();
	
	for(let i = 0; i < 10; i++) 
	{
		let obj = {
			name: 'Product ' + i,
			description: 'Lorem ipsum dolor sit amet',
			price: 102 + i,
			iso: 'USD',
			stars: 3,
			img: 'https://dummyimage.com/200x200/fff/000'
		};
	
		items.push(obj);
	}
</script>
<div class="text-center">
	<div class="bg-teal-800">
		<img
		src="data:image/png;base64,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"
		class="w-auto mx-auto bg-teal-800"
		alt="tailwindcss"
		/>
	</div>
</div>	
<div><Navegator/></div>
<div>
	<form class="flex gap-2 bg-orange-400">
		<Navbar let:hidden let:toggle>
			<div class="flex md:order-2  bg-orange-400">
				<Button data-collapse-toggle="mobile-menu-3" aria-controls="mobile-menu-3" aria-expanded="false" class="md:hidden text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 focus:outline-none focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 rounded-lg text-sm p-2.5" >
				<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 dark:text-white"><path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" /></svg>
				</Button>
				<div class="hidden relative md:block">
				<div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
					<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 dark:text-white"><path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" /></svg>
				</div>
				<Input id="search-navbar" class="pl-10" placeholder="Search..." />
				</div>
				<NavHamburger on:click={toggle} />
			</div>
			<NavUl {hidden}>
				<NavLi href="/" active={true}>Ciber Ofertas</NavLi>
				<NavLi href="/about">Only here!</NavLi>
				<NavLi href="/services">Gift Card</NavLi>
			</NavUl>
		</Navbar>
		<DarkMode />
	</form>
</div>
<Carru/>
<Foot/>