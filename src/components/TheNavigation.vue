<template>
  <nav
    ref="navbar"
    class="home-menu pure-menu pure-menu-horizontal pure-menu-fixed"
  >
    <a class="pure-menu-heading" href=""
      ><span>Sienna</span>Programming Contest</a
    >
    <ul class="pure-menu-list">
      <li class="pure-menu-item pure menu-selected">
        <router-link class="pure-menu-link" to="/">Home</router-link>
      </li>
      |
      <li class="pure-menu-item">
        <router-link class="pure-menu-link" to="about">About</router-link>
      </li>
    </ul>
  </nav>

  <span ref="hiddenSpan"></span>
</template>

<script setup>
import { ref, onMounted } from "vue";

const navbar = ref(null);
const hiddenSpan = ref(null);

onMounted(() => {
  const menuLinks = document.querySelectorAll(".pure-menu-link");
  console.log(menuLinks);
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.intersectionRatio > 0 && navbar.value !== null) {
        navbar.value.classList.remove("transition-nav-bgcolor");

        // Iterate thru menu links to change text color back
        menuLinks.forEach((item) => {
          item.classList.add("menu-color1");
          item.classList.remove("menu-color2");
        });
      } else if (navbar.value !== null) {
        navbar.value.classList.add("transition-nav-bgcolor");

        menuLinks.forEach((item) => {
          item.classList.add("menu-color2");
          item.classList.remove("menu-color1");
        });
      }
    });
  });

  observer.observe(hiddenSpan.value);
});
</script>

<style scoped>
/*
 * -- MENU STYLES --
 * I want to customize how my .pure-menu looks at the top of the page
 */

.home-menu {
  background: var(--nav-bg);
  font-family: var(--noto);
  padding: 0.5rem;
  text-align: left;
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.1);
  transition: 0.5s background ease-in;
}

.home-menu.transition-nav-bgcolor {
  background: rgba(162, 222, 208, 0.7);
}

.pure-menu-link {
  font-size: 1.2rem;
  transition: color 0.8s;
}

.menu-color1 {
  color: var(--sienna-green);
}

.pure-menu-item .menu-color1:hover {
  color: var(--sienna-green-hover);
}

.menu-color2 {
  color: #fff;
}

.pure-menu-item .menu-color2:hover {
  color: rgb(3, 68, 25);
}

.pure-menu.pure-menu-fixed {
  /* Fixed menus normally have a border at the bottom. */
  border-bottom: none;
  /* I need a higher z-index here because of the scroll-over effect. */
  z-index: 4;
}

.pure-menu-list {
  position: absolute;
  right: 0;
}

.home-menu .pure-menu-heading {
  color: white;
  font: 600 1.2rem var(--noto);
  margin-left: 5px;
  text-transform: none;
}

.home-menu .pure-menu-selected a {
  color: white;
}

.home-menu li a:hover,
.home-menu li a:focus {
  background: none;
  border: none;
  color: #aecfe5;
}

nav span {
  background: url("@/assets/images/siena-logo-green-sm.png") no-repeat;
  display: inline-block;
  position: relative;
  top: -8px;
  width: 90px;
  height: 29px;
  color: rgba(0, 0, 0, 0);
  margin-right: 15px;
}

span[ref="navbar"] {
  width: 0;
  height: 0;
}
</style>
