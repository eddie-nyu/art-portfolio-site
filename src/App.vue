<script setup lang="ts">
import { ref } from 'vue';
import { RouterLink, RouterView } from 'vue-router'

let isOpen = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
}

</script>

<template>
  <div>
    <header>
      <div class="wrapper">
        <nav id="navbar" class="navbar is-fixed-top is-transparent" role="navigation" aria-label="main navigation">
          <div class="navbar-brand">
            <a class="navbar-item">
              <RouterLink to="/">
                <img src="@/assets/jeff_Logo_black.svg" class="logo" alt="Jefford Castillo Logo" />
              </RouterLink>
            </a>

            <a role="button" :class="isOpen ? 'navbar-burger is-active' : 'navbar-burger'" aria-label="menu"
              aria-expanded="false" data-target="navbar" @click="toggleMenu">
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
            </a>
          </div>
          <div :class="isOpen ? 'navbar-menu is-active' : 'navbar-menu'">
            <div class="navbar-end">
              <!-- navbar items, navbar burger... -->
              <a class="navbar-item is-size-5">
                <RouterLink to="/">Work</RouterLink>
              </a>
              <a class="navbar-item is-size-5">
                <RouterLink to="/about">About</RouterLink>
              </a>
            </div>
          </div>
        </nav>
      </div>
    </header>
    <RouterView />
  </div>


</template>
