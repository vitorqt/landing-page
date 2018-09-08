<template>
    <navbar class="fixed-transparent-navbar" position="top" dark href="#" scrolling transparent>
      <mdb-navbar-brand href="https://mdbootstrap.com/" class="text-navson-logo">
        <img src="../assets/logo-navbar.png" height="27%" width="27%" />
      </mdb-navbar-brand>
      <navbar-collapse>
        <navbar-nav right>
          <router-link to="/"><navbar-item waves-fixed class="text-navson">INICIO</navbar-item></router-link>
          <router-link to="/sobre"><navbar-item waves-fixed class="text-navson">HISTÓRIA</navbar-item></router-link>
          <navbar-item href="#" waves-fixed class="text-navson">SERVIÇOS</navbar-item>
          <router-link to="/contato"><navbar-item waves-fixed class="text-navson">CONTATO</navbar-item></router-link>
          <navbar-item href="#" waves-fixed class="text-navson">PARCEIROS</navbar-item>
          <navbar-item href="#" waves-fixed class="text-navson">TRABALHE CONOSCO</navbar-item>
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

.text-navson {
  font-family: 'Courier New', Courier, monospace;
  font-size: 18px;
}
.text-navson-logo {
  font-family: 'Courier New', Courier, monospace;
  font-size: 30px;
}
</style>