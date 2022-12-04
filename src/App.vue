<template>
  <div>
    <SearchBar @searchTermChange="onSearchTermChange"></SearchBar>
    <VideoList></VideoList>
  </div>
</template>

<script>
import axios from "axios";
import SearchBar from "./components/SearchBar";
import VideoList from "./components/VideoList";

const apiKey = process.env.VUE_APP_API_KEY;

export default {
  name: "App",
  components: {
    SearchBar,
    VideoList
  },
  methods: {
    onSearchTermChange: function(searchTerm) {
      axios
        .get("https://www.googleapis.com/youtube/v3/search", {
          params: {
            key: apiKey,
            type: "video",
            part: "snippet",
            q: searchTerm
          }
        })
        .then(response => console.log(response));
    }
  }
};
</script>