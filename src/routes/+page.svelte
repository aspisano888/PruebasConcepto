<script>
	import Foot from './Food.svelte';
	import Carru from './Carru.svelte';
    import Navegator from './Navegator.svelte';
    import Navegator1 from './Navegator1.svelte';
	import Marcas from './Marcas.svelte';
	const imgUrl = new URL('../lib/images/logo.png', import.meta.url).href
</script>

<div class="relative"><Navegator/></div>
	<div>
		<div class="bg-teal-900 p-0">
			<div class="pt-20">
				<div class="bg-teal-700 flex justify-center">
					<img
					src="{imgUrl}"
					class="bg-teal-700 text-center"
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