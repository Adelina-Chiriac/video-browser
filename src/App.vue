<template>
  <div>
    <SearchBar @searchTermChange="onSearchTermChange"></SearchBar>
  </div>
</template>

<script>
import SearchBar from "./components/SearchBar";

export default {
  name: "App",
  components: {
    SearchBar
  },
  methods: {
    onSearchTermChange: function(searchTerm) {
      console.log(searchTerm);
    }
  }
};
</script>