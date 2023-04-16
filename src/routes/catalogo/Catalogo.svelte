<script>
    import Food from '../Food.svelte';
    import Navegator from '../Navegator.svelte';
    import { Card, Button, Rating, Badge } from "flowbite-svelte";
    let carro = [];
    let products = [
        {name: "manzana", image: "https://images-ti-vm1.tiendainglesa.com.uy/small/P018456-1.jpg?20221010160029,Manzana-Red-Deliciosa--Kg--en-Tienda-Inglesa", price: 95},
        {name: "naranja", image: "https://images-ti-vm1.tiendainglesa.com.uy/small/P090425-1.jpg?20211015030020,Naranja-VALENCIA-Malla-2-Kg-en-Tienda-Inglesa", price: 93},
        {name: "limón", image: "https://images-ti-vm1.tiendainglesa.com.uy/small/P019818-1.jpg?20190117160043,Lim%C3%B3n-Importado--Kg--en-Tienda-Inglesa", price: 72},
        {name: "cebolla", image: "https://images-ti-vm1.tiendainglesa.com.uy/small/P020515-1.jpg?20221201124059,Cebolla-Granel--Kg--en-Tienda-Inglesa", price: 48},
        {name: "banana", image: "https://images-ti-vm1.tiendainglesa.com.uy/small/P017844-1.jpg?20221104104756,Banana-Ecuador--Kg--en-Tienda-Inglesa", price: 55},
        {name: "tomate", image: "https://www.lovemysalad.com/sites/default/files/styles/image_415x281/public/tomates_-_vladimir_morozov.jpg?itok=1iCgrokf", price: 120},
        {name: "papa blanca", image: "https://www.herbazest.com/imgs/0/a/c/451775/papa.jpg", price: 50},
        {name: "zanahoria", image: "https://images-ti-vm1.tiendainglesa.com.uy/small/P065316-1.jpg?20220110160023,Zanahoria-Especial-DE-LA-CHACRA-1-Kg-en-Tienda-Inglesa", price: 40},
        {name: "mamao", image: "https://images-ti-vm1.tiendainglesa.com.uy/small/P021471-2.jpg?20210525165513,Mamao-Calimosa--Kg--en-Tienda-Inglesa", price: 200},
        {name: "pepino", image: "https://images-ti-vm1.tiendainglesa.com.uy/small/P000176-1.jpg?20211127110024,Pepino-Granel-TIENDA-INGLESA-1-Kg-en-Tienda-Inglesa", price: 65},

    ]

    const addToCarro = (product) => {
        alert(JSON.stringify(product))
    }
</script>

<Navegator/>
<div class="flex pt-20 sm-flex">
    <div class="bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
    <div class="grid grid-cols-3 md:grid-cols-4 gap-4">
        {#each products as product}
        
        <Card padding="none">
            <a href="/">
                <img class="h-auto p-8 rounded-t-lg" src="{product.image}"  alt="product"/></a>
                <div class="h-auto px-5 pb-5">
                    <a href="/">
                        <h4 class='h-auto text-xl font-semibold tracking-tight text-gray-900 dark:text-white'>{product.name}</h4>
                    </a>
                    <Rating rating="4" size="18" class="mt-2.5 mb-5">
                        <Badge slot="text" class="ml-3">4</Badge>
                    </Rating>
                    <div class="h-auto justify-between items-center">
                        <span class="h-auto text-4xl font-bold text-gray-900 dark:text-white">${product.price}</span>
                        <Button shadow="purple" gradient color="purple" class="h-auto font-medium rounded-lg text-sm text-center mr-2 mb-2" on:click={() => addToCarro(product)}>Agregar</Button>
                    </div>
                </div>
            </Card>
            {/each}
        </div>
        </div>
    </div>
<Food/>