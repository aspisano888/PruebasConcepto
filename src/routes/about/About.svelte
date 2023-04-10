<script>
    import Food from '../Food.svelte';
    import Navegator from '../Navegator.svelte';
    import { Card } from "flowbite-svelte";
    import { Img } from 'flowbite-svelte';
    
    let hCard = false;
</script>

<Navegator/>
<div  class="bg-gradient-to-r from-sky-500 to-indigo-500 mx-32">
  <div><h2 class="pt-32 px-20 text-teal-200 overline font-bold text-4xl">Cuchos' Market</h2></div>
  <div class="sm-flex" >
    <div class="sm-flex my-24 mx-64">
      <Card img="../imagenes/logoSm.png" href="/" horizontal reverse={hCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Nosotros</h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Somos una cadena de superemercados que ofrece los mejores productos del mercado a su hogar. Nos destacamos por cumplir las necesidades de nuestros clientes los 365 dias del año, en cualquier parte del pais.
        </p>
      </Card>
    </div>
    <div class="sm-flex mx-72 my-5 w-1/2 pb-20 pt-0">
      <Card padding="none" size="xl" class="flex-auto grid md:grid-cols-2">
        <figure class="flex flex-col justify-center items-center p-8 text-center bg-white rounded-t-lg border-b border-gray-200 md:rounded-t-none md:rounded-tl-lg md:border-r dark:bg-gray-800 dark:border-gray-700">
          <blockquote class="mx-auto mb-4 max-w-2xl text-gray-500 dark:text-gray-400">
            <h3 class="p-0 text-lg font-semibold text-gray-900 dark:text-white">Muy buena atención</h3>
            <p class="my-4 font-light">El personal es muy amable y tienen excelente disposición. Me siento muy a gusto."</p>
          </blockquote>
          <figcaption class="flex justify-center items-center space-x-3">
            <img class="w-9 h-9 rounded-full" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/karen-nelson.png" alt="Karen profile">
            <div class="space-y-0.5 font-medium dark:text-white text-left">
              <div>Ana Pérez</div>
            </div>
          </figcaption>
        </figure>
        <figure class="flex flex-col justify-center items-center p-8 text-center bg-white rounded-tr-lg border-b border-gray-200 dark:bg-gray-800 dark:border-gray-700">
          <blockquote class="mx-auto mb-4 max-w-2xl text-gray-500 dark:text-gray-400">
            <h3 class="p-0 text-lg font-semibold text-gray-900 dark:text-white">Gran variedad de productos,</h3>
            <p class="my-4 font-light">Si buscas una marca en especial, en Cucho's seguro la encontras."</p>
          </blockquote>
          <figcaption class="flex justify-center items-center space-x-3">
            <img class="w-9 h-9 rounded-full" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/roberta-casas.png" alt="Robert profile">
            <div class="space-y-0.5 font-medium dark:text-white text-left">
              <div>Roberta Cosas</div>
            </div>
          </figcaption>
        </figure>
        <figure class="flex flex-col justify-center items-center p-8 text-center bg-white rounded-bl-lg border-b border-gray-200 md:border-b-0 md:border-r dark:bg-gray-800 dark:border-gray-700">
          <blockquote class="mx-auto mb-4 max-w-2xl text-gray-500 dark:text-gray-400">
            <h3 class="p-0 text-lg font-semibold text-gray-900 dark:text-white">Excelente</h3>
            <p class="my-4 font-light">Muy cálido lugar."</p>
          </blockquote>
          <figcaption class="flex justify-center items-center space-x-3">
            <img class="w-9 h-9 rounded-full" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/jese-leos.png" alt="Jese profile">
            <div class="space-y-0.5 font-medium dark:text-white text-left">
              <div>Leo Camacho</div>
            </div>
          </figcaption>
        </figure>
        <figure class="flex flex-col justify-center items-center p-8 text-center bg-white rounded-b-lg border-gray-200 md:rounded-br-lg dark:bg-gray-800 dark:border-gray-700">
          <blockquote class="mx-auto mb-4 max-w-2xl text-gray-500 dark:text-gray-400">
            <h3 class="p-0 text-lg font-semibold text-gray-900 dark:text-white">Efficient Collaborating</h3>
            <p class="my-4 font-light">La mejor carne del condado."</p>
          </blockquote>
          <figcaption class="flex justify-center items-center space-x-3">
            <img class="w-9 h-9 rounded-full" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/joseph-mcfall.png" alt="joseph profile">
            <div class="space-y-0.5 font-medium dark:text-white text-left">
              <div>Jose McFall</div>
          </div>
          </figcaption>
        </figure>
      </Card>
    </div>
  </div>
</div>
<Food/>