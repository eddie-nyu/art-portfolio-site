<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
        <div class="navbar-brand">
          <!-- navbar items, navbar burger... -->
          <a class="navbar-item">
            <RouterLink to="/">Home</RouterLink>
          </a>
          <a class="navbar-item">
            <RouterLink to="/about">About</RouterLink>
          </a>
        </div>
      </nav>
    </div>
  </header>

  <RouterView />
</template>
