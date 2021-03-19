<template>

  <header class="header">
                <h1 class="title text-purple-400">Dad Jokes</h1>
        <nav class="navigation">
                  <ul class="">
          <li>
              <nuxt-link class="rounded-lg bg-purple-300" to="/">Home</nuxt-link>
          </li>
      </ul >
      <ul >
          <li >
              <nuxt-link class="rounded-lg bg-purple-300" to="/jokes">Jokes</nuxt-link>
          </li>
      </ul>
      <ul>
          <li>
              <nuxt-link class="rounded-lg bg-purple-300" to="/about">About</nuxt-link>
          </li>
      </ul>
        </nav>
  </header>

</template>

<script>
export default {
    name : 'AppHeader'
}
</script>

<style>
.header{
    display: grid;
    grid-gap: 2rem;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    /* margin-bottom: 1rem;
    padding-bottom: 1rem; */
    border-bottom: 1px solid #ccc;
}
.header .title{
    font-size: 3rem;

}
.navigation{
    display: flex;
    justify-content: space-around;
}
.header nav ul {
      list-style: none;
}
.header nav a {
    display: inline-block;
    color : #fff;
    padding: 0.3rem 1rem;
    text-decoration: none;
}
</style>