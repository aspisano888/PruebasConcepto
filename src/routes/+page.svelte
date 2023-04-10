<script>
	import Foot from './Food.svelte';
	import Carru from './Carru.svelte';
    import Navegator from './Navegator.svelte';
    import Navegator1 from './Navegator1.svelte';
	import Marcas from './Marcas.svelte';
	import { Img } from 'flowbite-svelte';
	
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
<div class="relative"><Navegator/></div>
	<div>
		<div class="bg-teal-800 p-20">
			<div class="pt-20">
				<div class="bg-teal-800 flex justify-center">
					<img
					src="./imagenes/logo.png"
					class="bg-teal-800 text-center"
					alt="cucho's"
					/>
			</div>
		</div>	
		<Navegator1/>
		<div><Carru/></div>
		<div class="bg-amber-100"><Marcas/></div>
	</div>
</div>
<Foot/>