<script>
        import { Gallery } from "flowbite-svelte";
        import { Card, Button, Rating, Badge } from "flowbite-svelte";

        let marcas = [
        {name: "Saman", image: "https://www.saman.uy/wp-content/uploads/2015/03/LogoSamanMedium.png"},
        {name: "Cousa", image: "http://www.cousa.com/images/logo-cousa.svg"},
        {name: "Coca-Cola", image: "https://graffica.info/wp-content/uploads/2023/02/cocacola-logo.jpeg"},
        {name: "EstrellaDeGalicia", image: "https://estrellagalicia.es/wp-content/uploads/2021/07/logotipo-estrella-galicia-copia.png"},
        {name: "J&J", image: "https://1000logos.net/wp-content/uploads/2021/04/Johnson-and-Johnson-logo-768x461.png"},
        {name: "Sensodyne", image: "https://1000logos.net/wp-content/uploads/2020/04/Sensodyne-Logo-768x432.png"},
        {name: "DeAmbrosi", image: "https://www.deambrosi.com.uy/wp-content/uploads/2020/07/alimentos-deambrosi.png"},
        {name: "Higenol", image: "https://s3.amazonaws.com/confort.c9/app/uploads/higienol-uruguay/2018/08/08132753/higienol_logo1.png"},
        {name: "Unilever", image: "https://assets.turbologo.com/blog/es/2021/09/22083444/unilever.png"},
        {name: "Schneck", image: "https://f.fcdn.app/assets/commerce/tienda.schneck.com.uy/747f_c435/public/web/img/logo.svg"},
    ]
</script>

<h4 class="text-center text-orange-700 underline decoration-double uppercase text-lg">Algunas marcas</h4>
<div class="grid grid-cols-5 gap-5">
    {#each marcas as marca}
    <Card padding="none">
        <a href="/"><img class="p-8 rounded-t-lg" src="{marca.image}"  alt="product"/></a>
    </Card> 
    {/each}
</div>