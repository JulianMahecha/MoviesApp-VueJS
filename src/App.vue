<template>
  <div id="app">
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand>Movies App</b-navbar-brand>
      <b-navbar-nav class="mx-auto">
        <b-nav-item active>
          <router-link to="/">Popular</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="top-rated">Top Rated</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="upcoming">Upcoming</router-link>
        </b-nav-item>
      </b-navbar-nav>
      <b-nav-form>
        <b-form-input size="sm" class="mr-sm-2" placeholder="Search" v-model="filter"></b-form-input>
        <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
      </b-nav-form>
    </b-navbar>
    <router-view />
  </div>
</template>

<style>
</style>
