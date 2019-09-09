<template>
  <div id="app">
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand>Movies App</b-navbar-brand>
      <b-navbar-nav class="mx-auto">
        <b-nav-item>
          <router-link to="/">Top Rated</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="top-rated">Popular</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="top-rated">Trending</router-link>
        </b-nav-item>
      </b-navbar-nav>
    </b-navbar>
    <router-view />
  </div>
</template>

<style>
</style>
