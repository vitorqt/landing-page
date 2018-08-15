<template>
    <!--Navbar-->
    <navbar class="indigo" dark>
        <!-- Navbar brand -->
        <mdb-navbar-brand href="https://mdbootstrap.com/">
            Navbar
        </mdb-navbar-brand>
        <navbar-collapse>
            <navbar-nav class="nav">
            <navbar-item active><router-link to="/">Home</router-link></navbar-item>
            <navbar-item><router-link to="/about">About</router-link></navbar-item>
            <!-- Dropdown -->
            <dropdown tag="li" class="nav-item">
                <dropdown-toggle tag="a" navLink color="indigo" slot="toggle" waves-fixed>Dropdown</dropdown-toggle>
                <dropdown-menu>
                <dropdown-item>Action</dropdown-item>
                <dropdown-item>Another action</dropdown-item>
                <dropdown-item>Something else here</dropdown-item>
                </dropdown-menu>
            </dropdown>
            </navbar-nav>
            <!-- Search form -->
            <form class="form-inline">
            <input class="form-control mr-auto p-2" type="text" placeholder="Search" aria-label="Search">
            </form>
        </navbar-collapse>
    </navbar>
</template>

<script>
import { Navbar, NavbarItem, NavbarNav, NavbarCollapse, Container, Dropdown, DropdownItem, DropdownMenu, DropdownToggle, MdInput, mdbNavbarBrand } from 'mdbvue';

export default {
  name: 'NavbarPage',
  components: {
    Navbar,
    NavbarItem,
    NavbarNav,
    NavbarCollapse,
    Container,
    Dropdown,
    DropdownItem,
    DropdownMenu,
    DropdownToggle,
    MdInput,
    mdbNavbarBrand
  }
};
</script>
