<template>
  <ul>
    Video List
  </ul>
</template>

<script>
import VideoListItem from "./VideoListItem";

export default {
  name: "VideoList",
  components: {
    VideoListItem
  },
  props: {
    videos: Array
  }
}
</script>

<style>
</style>