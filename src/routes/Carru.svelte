<script>
// @ts-nocheck

    import { Carousel, CarouselTransition } from 'flowbite-svelte'
    // ./imageData/+server.js has the following
    let showThumbs=false
    let showCaptions=false
    let imageHeight =300;
    let imageSpacing = 3;
    const images = [
    {
      id: 0,
      name: "Ofertas",
      imgurl: "data:image/jpeg;base64,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",
      attribution: "cosmic-timetraveler-pYyOZ8q7AII-unsplash.com",
      style: "height-{imageHeight}px margin right-{imageSpacing}px",
    },
    {
      id: 1,
      name: "Super ofertas",
      imgurl: "",
      attribution: "cristina-gottardi-CSpjU6hYo_0-unsplash.com",
      style: "h-{imageHeight}px mr-{imageSpacing}px",
    },
    {
      id: 2,
      name: "50%Off",
      imgurl: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRVB6PTlNtOisFm4LCVCPR0I4B4oYotcf-JIg&usqp=CAU",
      attribution: "johannes-plenio-RwHv7LgeC7s-unsplash.com",
      style: "h-{imageHeight}px mr-{imageSpacing}px",
    },
    {
      id: 3,
      name: "MuchosOff",
      imgurl: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTUR2PKkJM98WyYkCkBdaFpEZw7lDXRXrwQKQ&usqp=CAU",
      attribution: "jonatan-pie-3l3RwQdHRHg-unsplash.com",
      style: "h-{imageHeight}px mr-{imageSpacing}px",
    },
    {
      id: 4,
      name: "Oferta del dia",
      imgurl: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSx1sl0cvSgtpmJm4IwkuGMoFjzCRYqBg0vQA&usqp=CAU",
      attribution: "mark-harpur-K2s_YE031CA-unsplash",
      style: "h-{imageHeight}px mr-{imageSpacing}px",
    },
  ];
  </script>
  <div class="flex overflow-x-auto relative p-3 w-full bg-sky-400 justify-center" >
    <CarouselTransition {images} loop transitionType="fade" transitionParams="{{ duration: 2000 }}" showCaptions={false} showThumbs={false} duration="5000" />
  </div>


<!--
<div class="flex">
  <div class="flex overflow-x-auto relative p-3 w-full justify-center">
      {#each images as image (image.id)}
          <img
              src={image.imgurl}
              alt={image.name}
              id={image.id}
              style={`height: ${imageHeight}px; margin-right: ${imageSpacing}px `}
          />
      {/each}
  </div>
</div>

  <div class="flex overflow-x-auto relative p-3 w-full justify-center">
      <Carousel {images} loop {imageHeight} {imageSpacing} {showCaptions} {showThumbs} duration="3000"/>
  </div>
  <script>
 {images}  

    export let images;
    export let imageHeight = 150;
    export let imageSpacing = 0;
</script>

<div class="carousel">
    <div class="carousel__container">
        {#each images as image (image.id)}
            <img
                src={image.path}
                alt={image.alt}
                id={image.id}
                style={`height: ${imageHeight}px; margin-right: ${imageSpacing}px`}
            />
        {/each}
    </div>
</div>

<style>
    .carousel {
        display: flex;
        overflow-x: auto;
        position: relative;
        width: 100%;
    }
    .carousel__container {
        display: flex;
    }
</style>
-->
