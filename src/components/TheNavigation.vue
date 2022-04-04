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
</template>

<script setup>
/* import { ref } from "vue";
const observer = new IntersectionObserver(handleIntersection);

const target = ref("navbar");
observer.observe(target.value);
console.log(target); */

/* function handleIntersection(entries) {
  entries.map((entry) => {
    if (entry.isIntersecting) {
      entry.target.classList.add("transition-nav");
    } else {
      entry.target.classList.remove("transition-nav");
    }
  });
} */
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
}

.transition-nav {
  background-color: #fff;
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

.pure-menu-item .pure-menu-link {
  color: var(--sienna-green);
  font-size: 1.2rem;
  transition: color 0.8s;
}

.pure-menu-item .pure-menu-link:hover {
  color: var(--sienna-green-hover);
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
</style>
