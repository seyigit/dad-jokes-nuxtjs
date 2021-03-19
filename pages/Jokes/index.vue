<template>
  <div>
    <SearchJokes v-on:search-text="searchText" />
    <br />
    <br />
    <hr />
    <Joke
      v-for="joke in jokes"
      :key="joke.id"
      :id="joke.id"
      :joke="joke.joke"
    />
  </div>
</template>
<script>
import Joke from '@/components/Joke'
import SearchJokes from '@/components/SearchJokes'
export default {
  components: {
  Joke,
  SearchJokes
  },
  data (){
    return {
      jokes : [],
      text : ''
    }
  },
  async created (){
    const config = {
      headers :{
        'Accept': 'application/json'
      }
    }
    const res = await this.$axios.get("https://icanhazdadjoke.com/search",config)
    this.jokes = res.data.results;
  },
  methods : {
    async searchText(text){
           const config = {
      headers :{
        'Accept': 'application/json'
      }
    }
    const res = await this.$axios.get("https://icanhazdadjoke.com/search?term="+text,config)
    this.jokes = res.data.results;
    }
  },
  
head(){
    return {
        title : 'Dad Jokes',
        meta : [
            {
                hid: 'description',
                name : 'description',
                content : 'Best place for corny dad jokes'
            }
        ]
    }
}
}
</script>

<style>
</style>