<template>
  <form>
    <input class="border-purple-200 border-2 p-0.5" type="text" v-model="text" placeholder="Search Jokes" />
    <input class="bg-purple-300 text-white rounded p-1" @click.prevent="onSubmit" type="submit" value="Search Jokes" />
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