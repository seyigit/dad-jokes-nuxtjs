<template>

  <header class="header">
                <h1 class="title">Dad Jokes</h1>
        <nav class="navigation">
                  <ul>
          <li>
              <nuxt-link to="/">Home</nuxt-link>
          </li>
      </ul>
      <ul>
          <li>
              <nuxt-link to="/jokes">Jokes</nuxt-link>
          </li>
      </ul>
      <ul>
          <li>
              <nuxt-link to="/about">About</nuxt-link>
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
    color: #526488;

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
    background: #333;
    color : #fff;
    padding: 0.3rem 1rem;
    text-decoration: none;
}
</style>