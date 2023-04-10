<script>
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte'
  import Colllapse from './Colllapse.svelte';


  </script>

<Navbar let:hidden let:toggle>
  <Colllapse/> 

    <NavHamburger on:click={toggle} />
    <NavUl {hidden}>
      <NavLi href="/about">Gift card</NavLi>
      <NavLi href="/services">Only Here!</NavLi>
      <NavLi href="/pricing">Cyber Lunes</NavLi>
    </NavUl>
  </Navbar>