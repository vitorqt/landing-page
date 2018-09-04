<template>
    <navbar class="fixed-transparent-navbar" position="top" dark href="#" scrolling transparent>
      <mdb-navbar-brand href="https://mdbootstrap.com/">
       Navbar
      </mdb-navbar-brand>
      <navbar-collapse>
        <navbar-nav right>
          <router-link to="/"><navbar-item waves-fixed>INICIO</navbar-item></router-link>
          <navbar-item href="#" waves-fixed>HISTÓRIA</navbar-item>
          <navbar-item href="#" waves-fixed>SERVIÇOS</navbar-item>
          <router-link to="/contato"><navbar-item waves-fixed>CONTATO</navbar-item></router-link>
          <navbar-item href="#" waves-fixed>PARCEIROS</navbar-item>
          <navbar-item href="#" waves-fixed>TRABALHE CONOSCO</navbar-item>
        </navbar-nav>
      </navbar-collapse>
    </navbar>
</template>

<script>
import {
  Navbar,
  NavbarItem,
  NavbarNav,
  NavbarCollapse,
  Dropdown,
  DropdownItem,
  DropdownMenu,
  DropdownToggle,
  MdInput,
  Btn,
  mdbNavbarBrand
} from "mdbvue";

export default {
  name: "NavigationPage",
  components: {
    Navbar,
    NavbarItem,
    NavbarNav,
    NavbarCollapse,
    Dropdown,
    DropdownItem,
    DropdownMenu,
    DropdownToggle,
    MdInput,
    Btn,
    mdbNavbarBrand
  },
  data() {
    return {
      active: {
        0: false
      }
    };
  },
  methods: {
    toggleDropdown(index) {
      for (let i = 0; i < Object.keys(this.active).length; i++) {
        if (index !== i) {
          this.active[i] = false;
        }
      }
      this.active[index] = !this.active[index];
    },
    allDropdownsClose(target) {
      for (let i = 0; i < Object.keys(this.active).length; i++) {
        this.active[i] = false;
      }
    },
    onClick(e) {
      let parent = e.target;
      let body = document.getElementsByTagName("body")[0];
      while (parent !== body) {
        if (
          parent.classList.contains("dropdown") ||
          parent.classList.contains("btn-group")
        ) {
          return;
        }
        parent = parent.parentNode;
      }
      this.allDropdownsClose(e.target);
    }
  },
  mounted() {
    document.addEventListener("click", this.onClick);
  },
  destroyed() {
    document.removeEventListener("click", this.onClick);
  }
};
</script>

<style scoped>
.navbar .dropdown-menu a:hover {
  color: inherit !important;
}
.fixed-transparent-navbar {
  transition: 1s !important;
}
.fixed-transparent-navbar {
  background-color: #0b2b0b !important;
}
</style>