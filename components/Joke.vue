<template>
<nuxt-link :to="'jokes/' + id" tag="a">
  <div class="joke">
      <p>{{joke}}</p>
  </div>
  </nuxt-link>
</template>

<script>
export default {
    name : 'Joke',
    props : ['joke','id']
}
</script>

<style>
.joke {
    padding: 1rem;
    border: 1px solid #ccc ;
    margin: 1rem 0;
}
a{
    text-decoration: none;
    color: inherit;
}
</style>