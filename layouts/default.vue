<template>
  <div class="container">
    <AppHeader/>
    <main>
      <Nuxt />
    </main>
  </div>
</template>
<script>

import AppHeader from '@/components/AppHeader'


export default {
  components : {
    AppHeader
  }
}
</script>
<style>
*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
.container{
  max-width: 800px;
  margin: 0 auto;
  overflow: hidden;
  padding: 1rem 2rem;
  background: #fff;
}
body{
  background: #dde;
}
main{
  padding-top: 30px;
}
</style>
