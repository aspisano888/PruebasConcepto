<script>
// @ts-nocheck

    import { Carousel, CarouselTransition } from 'flowbite-svelte'

    const images = [
    {
      id: 0,
      name: "Ofertas",
      imgurl: "https://cdn.shopify.com/s/files/1/0229/0839/files/Blog_Banner.jpg?2814&width=1024",
      attribution: "cosmic-timetraveler-pYyOZ8q7AII-unsplash.com",
      style: "height-{imageHeight}px margin right-{imageSpacing}px",
    },
    {
      id: 1,
      name: "Super ofertas",
      imgurl: "https://www.salmantina.com/media/catalog/category/ofertas_1.jpg",
      attribution: "cristina-gottardi-CSpjU6hYo_0-unsplash.com",
      style: "h-{imageHeight}px mr-{imageSpacing}px",
    },
    {
      id: 2,
      name: "CyberLunes",
      imgurl: "https://www.exoticca.com/es/blog/wp-content/uploads/2021/11/930X360_Image-of-the-blog-pre-launch_ES-1.jpg",
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
      imgurl: "https://comefruta.es/wp-content/uploads/frutas-y-verduras-ecol%C3%B3gicas-1.png",
      attribution: "mark-harpur-K2s_YE031CA-unsplash",
      style: "h-{imageHeight}px mr-{imageSpacing}px",
    },
  ];
  </script>
  <div class="flex p-3 w-full bg-sky-400 justify-center" >
    <CarouselTransition {images} loop transitionType="fade" transitionParams="{{ duration: 2000 }}" showCaptions={false} showThumbs={false} duration="5000" />
  </div>