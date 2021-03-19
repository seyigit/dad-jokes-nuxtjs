<template>
  <form>
    <input type="text" v-model="text" placeholder="Search Jokes" />
    <input @click.prevent="onSubmit" type="submit" value="Search Jokes" />
  </form>
</template>

<script>
export default {
  name: "SearchJokes",
  data() {
    return {
      text: "",
    };
  },
  methods: {
    onSubmit() {
      this.$emit("search-text", this.text);
      this.text = "";
    },
  },
};
</script>

<style>
</style>