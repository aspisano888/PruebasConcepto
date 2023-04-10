<script>
  import { Navbar, NavLi, NavUl, NavHamburger } from 'flowbite-svelte'
	import { DarkMode } from 'flowbite-svelte';

</script>
<div class="fixed top-0 left-0 right-0">
  <Navbar let:hidden let:toggle class="bg-teal-900">
    <DarkMode />

    <NavHamburger on:click={toggle} />
    <NavUl {hidden}>
      <NavLi href="./" active={true}>Home</NavLi>
      <NavLi href="./about" class="text-amber-200">About</NavLi>
      <NavLi href="./catalogo" class="text-amber-200">Catalogo</NavLi>
      <NavLi href="./ofertas" class="text-amber-200">Ofertas</NavLi>
    </NavUl>
  </Navbar>
</div>

