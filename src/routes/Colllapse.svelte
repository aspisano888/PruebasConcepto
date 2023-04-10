<script>
    import { Button , Dropdown , DropdownItem , DropdownDivider , Chevron } from 'flowbite-svelte'
</script>

<Button gradient color="teal"><Chevron>Categorías</Chevron></Button>
<Dropdown class="bg-grey">
  <DropdownItem>Frescos</DropdownItem>
  <DropdownItem class="flex items-center justify-between"><Chevron placement="right">Almacén</Chevron></DropdownItem>
  <Dropdown placement="right-start">
    <DropdownItem>Arroz-Fideos-Harina</DropdownItem>
    <DropdownItem>Huevos</DropdownItem>
    <DropdownItem>Aceites-Aderezos</DropdownItem>
  </Dropdown>
  <DropdownItem>Congelados</DropdownItem>
  <DropdownItem class="flex items-center justify-between"><Chevron placement="right">Bebídas</Chevron></DropdownItem>
  <Dropdown placement="right-start">
    <DropdownItem>Con alchol</DropdownItem>
    <DropdownItem>Sin alcohol</DropdownItem>
  </Dropdown>
  <DropdownItem>Limpieza</DropdownItem>
  <DropdownItem>Perfumería</DropdownItem>
  <DropdownItem slot="footer">Sign out</DropdownItem>
</Dropdown>