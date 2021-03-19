<template>
  <div>
    <div>
        <nuxt-link to="/jokes">Back To Jokes</nuxt-link>
        <br><br>
        <h2 class="jokes">{{joke}}</h2>
        <br><br>
        <hr />
        <small>Joke ID : {{$route.params.id}}</small>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      joke: {},
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };
    const res = await this.$axios.get(
      'https://icanhazdadjoke.com/j/'+this.$route.params.id,
      config
    ).then(res => {
    this.joke = res.data.joke; // joke arrayine eşitlendi
    })
    
  },
  head(){
    return {
        title : this.joke,
        meta : [
            {
                hid: 'description',
                name : 'description',
                content : 'Best place for corny dad jokes'
            }
        ]
    }
}
};
</script>

<style scoped>
.jokes{
    border: 1px solid #ddd;
    padding: 10px;
}
</style>