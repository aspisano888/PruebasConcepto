<script>
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Skeleton } from 'flowbite-svelte'
  import * as Icon from 'svelte-heros-v2';
  import Colllapse from '../Colllapse.svelte';

</script>

<Navbar let:hidden let:toggle class="bg-teal-800">
  <Colllapse/> 
  <NavHamburger on:click={toggle} />
      <NavUl {hidden}>
      <NavLi href="./" active={true}>Home</NavLi>
      <NavLi href="./about" class="text-amber-100">About</NavLi>
      <NavLi href="./catalogo" class="text-amber-100">Catalogo</NavLi>
      <NavLi href="./ofertas" class="text-amber-100">Ofertas</NavLi>
      </NavUl>
  </Navbar>

