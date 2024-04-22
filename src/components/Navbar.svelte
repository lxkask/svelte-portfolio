<script lang="ts">
    import {
      Collapse,
      Navbar,
      NavbarToggler,
      NavbarBrand,
      Nav,
      NavItem,
      NavLink,
    } from '@sveltestrap/sveltestrap';

    let isOpen = false;
    import "../app.css";
    import "./Navbar.css"
</script>
  
<Navbar color="dark" theme="dark" expand="md" class="navbar">
    <NavbarBrand href="/" class="me-auto">
      <span class="navbar-text">Lukáš Kubík</span>
    </NavbarBrand>
    <NavbarToggler on:click={() => (isOpen = !isOpen)} />
    <Collapse {isOpen} navbar expand="md">
      <Nav class="ms-auto" navbar>
        <NavItem class="text-xl">
          <NavLink href="/contact">
            <span class="navbar-link">Contact</span>
          </NavLink>
        </NavItem>
      </Nav>
    </Collapse>
</Navbar>
